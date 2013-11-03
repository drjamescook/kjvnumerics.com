KJVNumerics.com
========================

This project is in it's initial startup phase. The intention is to turn kjvnumerics.com into a full fledge application
in which users can search out the numerical meaning in the King James Version of the Bible.

I am making the project public because I think something like this should be available to everyone.

I also would like people's ideas and help if anyone wishes to do so. The application will be built with PHP for the
backend, MySQL for the database, and will use [Sencha ExtJS] [1] framework extensively for the front end.

Please be patient with me while I get the project setup.

Project Structure
--------------------

* kjvnumerics.com -> /ui/build/production/KJVN
* api.kjvnumerics.com -> /api/public

[Restler] [2] is the framework I will be using for the PHP backend.

Here is my windows hosts files configuration.

    # For the KJV Numerics project.
    127.0.0.1 kjvnumerics.com.localhost
    127.0.0.1 api.kjvnumerics.com.localhost
    127.0.0.1 ui.kjvnumerics.com.localhost

Apache httpd-vhosts.conf file.

    NameVirtualHost *:80

    <VirtualHost *:80>
        ServerAdmin webmaster@kjvnumerics.com
        DocumentRoot "C:/webserver/htdocs/kjvnumerics.com/ui/build/production/KJVN"
        ServerName kjvnumerics.com.localhost
        ServerAlias www.kjvnumerics.com.localhost
        ErrorLog "logs/kjvnumerics.com-error.log"
        CustomLog "logs/kjvnumerics.com-access.log" common
    </VirtualHost>

    <VirtualHost *:80>
        ServerAdmin webmaster@kjvnumerics.com
        DocumentRoot "C:/webserver/htdocs/kjvnumerics.com/api"
        ServerName api.kjvnumerics.com.localhost
        #ServerAlias api.kjvnumerics.com.localhost
        ErrorLog "logs/api.kjvnumerics.com-error.log"
        CustomLog "logs/api.kjvnumerics.com-access.log" common
    </VirtualHost>

    <VirtualHost *:80>
        ServerAdmin webmaster@kjvnumerics.com
        DocumentRoot "C:/webserver/htdocs/kjvnumerics.com/ui"
        ServerName ui.kjvnumerics.com.localhost
        #ServerAlias ui.kjvnumerics.com.localhost
        ErrorLog "logs/ui.kjvnumerics.com-error.log"
        CustomLog "logs/ui.kjvnumerics.com-access.log" common
    </VirtualHost>


  [1]: http://www.sencha.com/products/extjs/ "Sencha ExtJS"
  [2]: https://github.com/Luracast/Restler "Restler"