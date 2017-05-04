dodać subdomenę widoczna w katalogu domains należy: Zarządzanie domeną -> Dodaj dodatkową domenę

#jeśli jeszcze nie dodalem SSH klucza z githhubem lub bitbucketem
ssh-keygen -t rsa
cat ~/.ssh/id_rsa.pub

# Login without password:
ssh-copy-id "mario199@85.17.23.18" -p 59184

rails new APPNAME -d postgresql
bundle install
rake db:setup
git init
git add . && git commit -m "init"
git remote add origin git@github.com:blaszczakphoto/linuxpl_test_rails.git
git push -u origin master

rvm user rubies;
rvm user all;

mozna tez od razu załadowac zmienne lokalne:
source $HOME/.rvmrc

rvm autolibs disable

rvm install 2.4.0
rvm gemset create APPNAME
rvm gemset use app1																																			
rvm gemdir

cd /usr/home/mario199/domains/rails.mario199.usermd.net
git pull HTTPURL
# gem install bundler
gem install bundler -v '< 1.12' 
bundle install

STWORZYĆ postgresql DB w panelu admina
vim /home/mario199/.bashrc
add on the end of the file:
export APP_NAME_DATABASE_FILE=CHANGE_PASSWORD

rake db:migrate RAILS_ENV="production" 

rake secret
vim /home/mario199/.bashrc
source /home/mario199/.bashrc

RAILS_ENV=production bin/rails assets:precompile

kill -9 $(cat tmp/pids/server.pid) && ruby bin/rails server webrick -e production -p 3010 -d
ruby bin/rails server webrick -e production -p 3010 -d

ps aux | grep rails
kill -9 PID

Gemfile
gem 'capistrano', '~> 3.6'
gem 'capistrano-rails', '~> 1.2'
gem 'capistrano-rvm'

/home/mariusz/Projects/Ruby/test_linuxpl/config/deploy/production.rb web_server_port rvm_custom_path rvm_ruby_version
/home/mariusz/Projects/Ruby/test_linuxpl/config/deploy.rb application repo_url deploy_to assets_roles keep_releases default_shell after

cap production deploy


admin@linuxpl.com
prośba o przekierowanie aplikacji rails na domenę 
Witam,
w końcu udało mi się uruchomić aplikację rails pod adresem: http://85.17.23.18:3010/
Czy można prosić o przekierowanie jej na adres: rails.mario199.linuxpl.info?

