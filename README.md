# Redmine

Redmine is a flexible project management web application written using Ruby on Rails framework.

More details can be found in the doc directory or on the official website http://www.redmine.org

## Running with `docker-compose`

First, in a shell, start `mysql-server`:

```bash
docker-compose up
```

In another shell window,

```bash
export RBENV_VERSION=2.3.3 # if using rbenv to set ruby version
export RACK_ENV=production
export IMMUNIO_HELLO_URL=https://agent-stg.immun.io
export IMMUNIO_KEY=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
export IMMUNIO_SECRET=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
export IMMUNIO_LOG_LEVEL=debug
export IMMUNIO_CODE_PROTECTION_PLUGINS_ENABLED=true
export IMMUNIO_AGENT_VERSION=1.1.15

bundle
bundle exec rake db:create db:migrate

# Clear logs
bundle exec rake log:clear
> log/immunio.log

bundle exec rails s
```
