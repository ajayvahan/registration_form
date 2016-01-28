Registration form task
======================

Note: Please keep the 'app' and 'static' folder inside '/var/www/cgi-bin/task/' directory and make 
sure that your Web Server supports CGI and it is configured to handle CGI Programs.

Packages reqiured to run:
-----------------------

1. MySQLdb
2. cgi
3. validate_email

path required to run in terminal:
------------------------------

 1.for python files:
    
    /var/www/html/cgi-bin/task/app/filename.py

2.for html,html_data

    /var/www/html/cgi-bin/task/static/html/filename.html
   
path reqiured to run in browser:
---------------------------------

   http://localhost/cgi-bin/task/static/html/login.html
 
 
CGI configuration :-
---------------------------------------------------
serve-cgi-bin.conf

	< Directory "/var/www/html/cgi-bin" >
		AddHandler cgi-script .cgi .py
		AllowOverride None
		Options +ExecCGI -MultiViews +SymLinksIfOwnerMatch
		Require all granted
	< /Directory >
  

 
