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

### other
- docker-compose for later in the development
- pulumi for iac

caching


### poc folder structure
```
.
├── Dockerfile
├── controller
│   ├── *-controller.go
│   └── *-controller_test.go
├── entity
│   └── *-entity.go
├── utils
│    └── errors
│        └── *-error.go
├── go.mod
├── go.sum
├── infrastructure
│   ├── middleware
│   │   └── *-middleware.go
│   ├── router
│   │   ├── *-router.go
│   │   └── router-interface.go
│   └── pulumi 
├── repository
│   └── *-repository.go
├── server.go
├── service
│   ├── *-service.go
│   └── *-service_test.go
└── tmp
    ├── build-errors.log
    └── main

.air.toml
.vscode/workflows/publish-docker.yml
/dto
/utils/validatior
.ebignore
Buildfile
Dockerfile
/infrastructure/database/database.go

```
