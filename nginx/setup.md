# Nginx Webserver

Used to serve static files, and other basic stuff.

The `config` directory is filled with config files. A default one has been provided, as a catchall.

The `www` directory is used to put files to serve.

A simple config looks like
```conf
server {

    listen       80;
    listen  [::]:80;
    server_name  shorty.systems;

    root /www/home;

    location / {
        try_files $uri $uri/ $uri.html =404;
    }
}

```