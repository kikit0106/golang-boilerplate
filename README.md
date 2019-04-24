# golang-boilerplate

Simple golang boilerplate for building API

### How to Run

1. Install all project dependencies

```
make install-dep
```

2. Generate gobindata for migrations

```
make generate-migration
```

3. Create new database
4. Run this project

```
go run main.go -listen-port="9000" -db-url="postgres://postgres:postgres@localhost:5432/golang-simple-crud?sslmode=disable" -debug="true"
```

### List of Routes

The application runs as an HTTP server at port 9000 (default). It provides some endpoints:

- `GET /api/v1/users`: get all users
- `GET /api/v1/users/:id`: get detail a user by id
- `POST /api/v1/users`: creates a new user
- `PUT /api/v1/users/:id`: update a user by id
- `DELETE /api/v1/users/:id`: delete a user by id

## Built With

- [Gin](https://github.com/gin-gonic/gin) - HTTP web framework
- [Pg](https://github.com/go-pg/pg) - Golang ORM with focus on PostgreSQL features and performance
- [Sql-migrate](https://github.com/rubenv/sql-migrate) - SQL schema migration tool
- [Go-bindata](https://github.com/shuLhan/go-bindata) - Embedding binary data in a Go program
