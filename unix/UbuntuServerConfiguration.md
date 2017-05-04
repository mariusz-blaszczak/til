`adduser deploy`
`gpasswd -a deploy sudo`

#log in as deploy
#ssh-copy-id
https://patrickmn.com/aside/how-to-keep-alive-ssh-sessions/


#fix locales error:
`sudo locale-gen en_US en_US.UTF-8 pl_PL pl_PL.UTF-8`
`sudo dpkg-reconfigure locales`

https://www.digitalocean.com/community/tutorials/how-to-install-ruby-on-rails-with-rbenv-on-ubuntu-16-04

https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-16-04
...
`sudo apt-get install mysql-server mysql-client libmysqlclient-dev`

`mysql -p -u root`

```sql
CREATE USER 'm1210_test'@'localhost' IDENTIFIED BY '7mtmwCFl';
create database m1210_test;
GRANT ALL PRIVILEGES ON * . * TO 'm1210_test'@'localhost';
```


https://gorails.com/deploy/ubuntu/16.04

```
mkdir -p ~/domains/mario199rails.ml
cd ~/domains/mario199rails.ml
```

https://www.phusionpassenger.com/library/walkthroughs/deploy/ruby/ownserver/nginx/oss/install_language_runtime.html

```
sudo vim /etc/nginx/passenger.conf
passenger_ruby /home/deploy/.rbenv/shims/ruby;
```

#shared_files and #dirs 
https://www.phusionpassenger.com/library/deploy/nginx/automating_app_updates/ruby/#setting-up-a-basic-directory-structure
```
cd /etc/nginx/sites-enabled
ln -s ../sites-available/app_name app_name
rm -rf default
sudo service nginx restart
```

https://www.digitalocean.com/community/tutorials/how-to-set-up-a-host-name-with-digitalocean


