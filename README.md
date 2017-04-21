# Redmine

Redmine is a flexible project management web application written using Ruby on Rails framework.

More details can be found in the doc directory or on the official website http://www.redmine.org

## Running in Vagrant/VMWare-fusion

```
cd /vagrant
bundle
bundle exec rake db:create
bundle exec rake db:migrate

export REDMINE_SECRET_TOKEN='012345678901234567890123456789012345678901234567890123456789'
export IMMUNIO_HELLO_URL=https://agent-stg.immun.io
export IMMUNIO_LOG_LEVEL=debug
export IMMUNIO_CODE_PROTECTION_PLUGINS_ENABLED=true
export IMMUNIO_KEY=xxxxxxxxxxxxxxxxxxxxxxxx
export IMMUNIO_SECRET=xxxxxxxxxxxxxxxxxxxxxxxxxxxx

bundle exec rails s -b 192.168.84.xxx
```
