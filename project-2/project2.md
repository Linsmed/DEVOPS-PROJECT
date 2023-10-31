# WEB STACK IMPLEMENTATION (LEMP STACK)

# STEP 1 - INSTALLATION OF NGINX WEB SERVER

- I started off by updating my server’s package index by running this command:
  `sudo apt update`
  ![sudAptUpdate](./images/sudo-apt-update.PNG)

- Afterwards,I installed Nginx using apt package:
  `sudo apt install nginx`

![sudo-apt-install](./images/nginx-install-yes.PNG)

- I entered yes, and got my nginx installed as shown below

![alt text](./images/nginx-install-final.PNG)

- To verify that nginx was successfully installed and is running as a service in Ubuntu, I ran:

`sudo systemctl status nginx`

![alt text](./images/verify-nginx-install.PNG)

- I accessed it locally in my Ubuntu shell, by running:

`curl http://localhost:80`

![alt text](./images/ubuntu-access.PNG)

- To test how our Nginx server can respond to requests from the Internet. I opened chrome to access following url:
  `http://54.226.16.249/`

![alt text](./images/Chrome-url-access.PNG)
