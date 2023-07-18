Nginx Ubuntu Installation
Update Packages

sudo apt-get update
Install Nginx

sudo apt-get install nginx
Verify Installation

sudo nginx -v
Start Nginx Server

nginx
Now visit http://localhost:80 and you would be able to see default nginx welcome page.

Nginx Docker Installation
Run Docker Ubuntu Image

docker run -it -p 8080:80 ubuntu
Update Packages

sudo apt-get update
Install Nginx

sudo apt-get install nginx
Verify Installation

sudo nginx -v
Start Nginx Server

nginx
Now visit http://localhost:8080 and you would be able to see default nginx welcome page.

Nginx Conf File
Install VIM

sudo apt-get install vim
Open nginx.conf file

vim etc/nginx/nginx.conf
Type Sample Nginx Conf

events {
}

http {
  server {
    listen 80;
    server_name _;
    
    location / {
      return 200 "Hello from Nginx Sever";
    }
  }
}
Reload Nginx

nginx -s reload
Visit localhost:8080 or localhost:80 and you should see Hello from Nginx Sever on browser.
