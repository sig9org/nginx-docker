# nginx-docker

This is [Nginx](https://nginx.org/en/) container image. Nginx is described on the official website as follows:

> nginx [engine x] is an HTTP and reverse proxy server, a mail proxy server, and a generic TCP/UDP proxy server, originally written by Igor Sysoev. For a long time, it has been running on many heavily loaded Russian sites including Yandex, Mail.Ru, VK, and Rambler. According to Netcraft, nginx served or proxied 22.36% busiest sites in November 2021. Here are some of the success stories: Dropbox, Netflix, Wordpress.com, FastMail.FM.

## Usage

## Exposing external port

```
docker run --detach --tty --publish 8080:80 --name nginx sig9/nginx
```

Then you can hit `http://localhost:8080` or `http://ADDRESS:8080` in your browser.

## Hosting some simple static content

```
docker run --detach --tty --publish 8080:80 --volume ${PWD}/html:/usr/share/nginx/html --name nginx sig9/nginx
```
