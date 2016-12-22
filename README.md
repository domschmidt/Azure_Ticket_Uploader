# ticket_uploader

 Data directory
 
 Data directory separation pattern
 
 SQL Connection
 
 Max uploadsize per file
 
 File extensions
 
 Ticket lifetime
 
 Ticket invalidation after successful upload
 
 Upload hash verification

# Web.config
Conf example:
```
<appSettings>
  <add key="data_dir" value="C:/temp/"/>
  <add key="data_dir_separation_pattern" value="{owner_id}/{ticket_id}/"/>
  <add key="sql_connection" value="Data Source=.\MSSQLSERVER2008; Initial Catalog=myDb;Integrated Security=SSPI;User ID=useradmin; Password=pass;"/>
  <add key="max_size" value="512M"/>
  <add key="file_extensions" value="zip,mp4,rar,7z"/>
  <add key="ticket_lifetime" value="2d"/>
  <add key="ticket_invalidation_after_upload" value="true"/>
  <add key="upload_verification" value="true"/>
</appSettings>
```

# Tickets (Entities)
Name

Email (Owner/Uploader)

Creationdate

# Technologies
ASP.Net App

ORM SQL Connections

2 main modules:
- Ticket creater
- Upload service

# Ticket creator
User (AD?)

Create new tickets

# Upload service
Validates Tickets

File selection + upload button

Upload progress

TCP segmented connection (as stable and performant as possible)

Session refresh for large uploads

