# blog-hexo
使用hexo搭建的个人博客，主题使用的是next，博客地址  https://shownmmp.top
## 安装环境
### 安装nodejs
```Bash
sudo apt-get install nodejs
sudo apt install nodejs-legacy
sudo apt install npm
#更换为淘宝镜像
sudo npm config set registry https://registry.npm.taobao.org
 ```
 ### 安装更新版本的工具N
 ```Bash
sudo npm install n -g
sudo n stable
```
### 安装hexo
sudo npm install -g hexo
## 部署到阿里云
```Bash
git clone https://github.com/wqh0109663/blog-hexo.git
```
### 安装nginx
```Bash
sudo apt-get install nginx
```
### 配置vim /etc/nginx/nginx.conf,直接贴上我的配置
```Bash
user root;
worker_processes auto;
pid /run/nginx.pid;

events {
        worker_connections 768;
        # multi_accept on;
}

http {
        server {
        server_name shownmmp.top www.shownmmp.top;
        charset utf-8;


        location / {
            root   /root/blog/public;
            index  index.html index.htm index.txt;
            error_page  404  /404.html;
        }

        #error_page  404              /404.html;

        # redirect server error pages to the static page /50x.html


    listen 443 ssl; # managed by Certbot
    ssl_certificate /etc/letsencrypt/live/shownmmp.top/fullchain.pem; # managed by Certbot
    ssl_certificate_key /etc/letsencrypt/live/shownmmp.top/privkey.pem; # managed by Certbot
    include /etc/letsencrypt/options-ssl-nginx.conf; # managed by Certbot
    ssl_dhparam /etc/letsencrypt/ssl-dhparams.pem; # managed by Certbot


}
##

sendfile on;
tcp_nopush on;
tcp_nodelay on;
keepalive_timeout 65;
types_hash_max_size 2048;
# server_tokens off;

# server_names_hash_bucket_size 64;
# server_name_in_redirect off;

include /etc/nginx/mime.types;
default_type application/octet-stream;

##
# SSL Settings
##

ssl_protocols TLSv1 TLSv1.1 TLSv1.2; # Dropping SSLv3, ref: POODLE
ssl_prefer_server_ciphers on;

##
# Logging Settings
##

access_log /var/log/nginx/access.log;
error_log /var/log/nginx/error.log;

##
# Gzip Settings
##

gzip on;
gzip_disable "msie6";

# gzip_vary on;
# gzip_proxied any;
# gzip_comp_level 6;
# gzip_buffers 16 8k;
# gzip_http_version 1.1;
# gzip_types text/plain text/css application/json application/javascript text/xml application/xml application/xml+rss text/javascript;

        ##
        # Virtual Host Configs
        ##

        include /etc/nginx/conf.d/*.conf;
        include /etc/nginx/sites-enabled/*;

        server {
    if ($host = www.shownmmp.top) {
        return 301 https://$host$request_uri;
    } # managed by Certbot


    if ($host = shownmmp.top) {
        return 301 https://$host$request_uri;
    } # managed by Certbot


        listen 80;
        server_name shownmmp.top www.shownmmp.top;
    return 404; # managed by Certbot




}}

```
### 配置https
参考我的地址[https://shownmmp.top/2018/10/11/nginx%E9%85%8D%E7%BD%AEhttps/](https://shownmmp.top/2018/10/11/nginx%E9%85%8D%E7%BD%AEhttps/)


### 遇到的几个问题
[https://shownmmp.top/2018/10/09/%E9%98%BF%E9%87%8C%E4%BA%91%E6%90%AD%E5%BB%BAhexo%E5%8D%9A%E5%AE%A2/](https://shownmmp.top/2018/10/09/%E9%98%BF%E9%87%8C%E4%BA%91%E6%90%AD%E5%BB%BAhexo%E5%8D%9A%E5%AE%A2/)
