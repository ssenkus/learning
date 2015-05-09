# Vhosts

## Edit `/etc/hosts` and add Private IP address

```
xxx.xxx.xxx.xxx www.myexample.local
```

## Create directory /var/www/html/myexample

```
mkdir /var/www/html/myexample
```

## Create vhost file
A good way to name it is to match the URL + .conf

```
nano /etc/nginx/sites-enabled/www.myexample.local.conf
```

Add this to the file:

```
## Defines vhost server
server {
        # liste on port 80, ipv4
        listen 80;

        # root filesystem of our domain
        root /var/www/html/myexample;

        # index file defaults
        index index.html index.htm index.php;

        # name of server, plus alias(es)
        server_name www.myexample.local myexample;

}
```
## Test nginx configuration

```
nginx -t
```


## Restart nginx
```
sudo service nginx restart
```


