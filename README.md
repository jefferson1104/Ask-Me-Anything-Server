# TERN

https://github.com/jackc/tern

## Tern commands

```bash
# Install
$ go install github.com/jackc/tern/v2@latest

# init tern
$ tern init ./internal/store/pgstore/migrations

# create migrations
$ tern new --migrations ./internal/store/pgstore/migrations migration_name

# run migration

```

## Fix to run `tern` on macbook

```bash
$ go env GOPATH
$ export PATH=$PATH:$(go env GOPATH)/bin
$ tern version
```
