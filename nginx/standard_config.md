# Standard Config

## Installing nginx on Ubuntu

```bash
sudo apt-get update
sudo apt-get install nginx
```

## Testing http via Lynx

```bash
sudo apt-get install lynx
```

## Upgrading to latest stable on Ubuntu


### Check version

```
nginx -v
```

### Create Backup

```
sudo cp /etc/nginx/nginx.conf /etc/nginx/nginx.conf.1.xx.xx.backup
```


### Stop Nginx
```
sudo service nginx stop
```

### Install dependencies

```
sudo aptitude install python-software-properties
```

### Add the repository for the stable version of Nginx


sudo add-apt-repository ppa:nginx/stable


### 

```
sudo service nginx restart
```


### Check version to verify update

```
nginx -v
```