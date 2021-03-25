# my-go-project-setup-2021

### prerequisite
- Homebrew is installed
- go is installed
- VS Code is installed
- Go extention for go is installed
- Docker is installed

### install air
```
go get -u github.com/cosmtrek/air
```

set alias in ~.zshrc
```
alias air='$(go env GOPATH)/bin/air'
```

### install awscli and ebcli
- https://aws.amazon.com/cli/
- https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/eb-cli3.html
- (install anyenv, pyenv, and python 3.7 if needs to be)

### init
```
go mod init
```

### Docker
```
docker build -t $PROJECT_NAME .
docker run -p $PORT:$PORT $PROJECT_NAME

```

### redis
- install redis from homebrew
```
redis-server
```

### postgres
- install postgres from homebrew
```
createdb $DB_NAME
```

### github actions
- create Publish-Docker-Github-Action
