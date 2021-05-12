# go-in-memory-server-test

A basic HTTP server for ordering pizzas. The server is tested using the Go package `net/http/httptest`.

I came accross this excellent blog post https://ieftimov.com/post/testing-in-go-testing-http-servers/ while ramping up my Go skills.

The API has three endpoints:

1. List all pizzas: GET /pizzas
2. Order a pizza : POST /orders
3. List all orders: GET /orders

## Test endpoints:

`curl -X POST localhost:8080/orders -d '{"pizza_id":1,"quantity":0}'`

`curl -X GET localhost:8080/pizzas`

`curl -X GET localhost:8080/orders`

`curl -X POST localhost:8080/orders -d '{"pizza_id":1,"quantity":4}'`

`curl -X GET localhost:8080/orders`
