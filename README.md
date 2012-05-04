# sensu heroku example app

This is an example app how to run [sensu]() on [Heroku]().

## Setup
Initialize the heroku app
```
heroku create --stack cedar
heroku addons:add redistogo
heroku addons:add rabbitmq
git push heroku master
```

## Configuration
The app reads all `*.json` config files on startup. So all configuration can be
dropped in there. By default the sensu server is started. If you want to run
the api, change the executable in `Procfile` to `sensu-api`.





[Heroku]: http://heroku.com
[sensu]: https://github.com/sensu/sensu
