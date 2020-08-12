
cd /etc/httpd/conf.d

sudo vi your_website.com.conf

<VirtualHost *:80>
    DocumentRoot "/var/www/html/your_website.com/public"
    ServerName www.your_website.com
    ServerAlias your_website.com
    <Directory "/var/www/html/your_website.com/public">
    Options FollowSymLinks
    AllowOverride All
    Options -Indexes
    </Directory>
</VirtualHost>
