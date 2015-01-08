## Simple Go server

Very simple Go lang server which prints out "Hello world"

purpose is to test how to build and deploy a web app to heroku

## Build process

Initialize git repo inside this project directory

```golang
go get github.com/kr/godep
```

```golang
godep save
```
Commit dependencies and then push to heroku:

```shell
heroku create -b https://github.com/kr/heroku-buildpack-go.git

git push heroku master

heroku config:set PORT=5000

heroku restart

heroku ps

heroku logs --tail
```
