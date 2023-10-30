NETCAT

netcap -op -h -puerto


nc -l -p 80 

nc *ip* *puerto*

Chat modo servidor

ncat -l *port*

Chat modo cliente

nc -c *ip* *port*


----------------------------------------------------
lsof -> conocer los puertos abriertos del sistema 
lsof -l -P -n
lsof -l -P -n | grep LISTEN

netstat PUTONA
netstat PUTONA | grep 80

escane la red y muestra los equipos
nmap -sn ip/mask
sudo nmap -sS *ip*

mkfifo /tmp/pipe; sh /tmp/pipe | netcat -v -l -p 2508> /tmp/pipe
nc *ip* *port*