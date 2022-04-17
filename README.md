## Requirements
1. Git: https://git-scm.com/
2. Vagrant:https://www.vagrantup.com/
3. Oracle VM VirtualBox manager: https://www.virtualbox.org/

## How to install & run 
 - Clone project
 ``` sh
$ git clone https://github.com/kobiShenkar/vagrant-ubuntu-nginx.git
````
 - Enter the vagrant-ubuntu-nginx folder
 ``` sh
$ cd vagrant-ubuntu-nginx
````
 - Run Vagrantfile
 ``` sh
$ vagrant up
````
 - Enter the served website by nginx
 ``` sh
host machine: localhost:8080
guest vm: $ curl localhost
````

- Make ssl certificate
 ``` sh
$ sudo mkdir /etc/nginx/ssl
$ openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/nginx/ssl/private.key -out /etc/nginx/ssl/public.pem
````

- copy config file
 ``` sh
$ vim /etc/nginx/conf.d
$ copy here default.conf
````
