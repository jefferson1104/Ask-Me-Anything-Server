# TERN

https://github.com/jackc/tern

## Fix to run `tern` on macbook

```bash
$ go env GOPATH
$ export PATH=$PATH:$(go env GOPATH)/bin
$ tern version
```

## Tern commands

```bash
# Install
$ go install github.com/jackc/tern/v2@latest

# init tern
$ tern init ./internal/store/pgstore/migrations

# create cmd godotenv
https://github.com/joho/godotenv

# create migrations
$ tern new --migrations ./internal/store/pgstore/migrations migration_name

# Create your terndotenv config file and your migration cmd

# execute this command to install packages in your project
$ go mod tidy

# run migration after create cmd
$ go run ./cmd/tools/terndotenv/main.go
```

# SQL C

https://docs.sqlc.dev/en/stable/overview/install.html

```bash
# Install using Go
$ go install github.com/sqlc-dev/sqlc/cmd/sqlc@latest

# create your file config sqlc.yaml

# generate from configuration file
$ sqlc generate -f ./internal/store/pgstore/sqlc.yaml

# execute this command to install packages in your project
$ go mod tidy

```

# GO GENERATE

create a gen.go file with this content

```go
package gen

//go:generate go run ./cmd/tools/terndotenv/main.go
//go:generate sqlc generate -f ./internal/store/pgstore/sqlc.yaml
```

execute this command

```bash
$ go generate ./...
```
