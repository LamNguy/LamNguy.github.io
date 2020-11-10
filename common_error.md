Placement error
vi /etc/httpd/conf.d/00-placement-api.conf
```
<Directory /usr/bin>
    <IfVersion >= 2.4>
        Require all granted
    </IfVersion>
    <IfVersion < 2.4>
        Order allow,deny
        Allow from all
    </IfVersion>
</Directory>
```

and restart service
