# Go Lang - Simple Blockchain Project

## How to run this project locally?
1. run ```go mod tidy```
2. run ```go run main.go -cmd <PORT_NUMBER>```

Start Multiple Nodes Together.

APIs

1. Create New Book
```
curl --location --request POST 'localhost:3000/new' \
--header 'Content-Type: application/json' \
--data-raw '{
    "title": "Book1",
    "author": "Vipul Panchal",
    "isbn": "111111",
    "publish_date": "2022-06-03"
}'
```

2. Create New Block
```
curl --location --request POST 'localhost:3001' \
--header 'Content-Type: application/json' \
--data-raw '{
    "book_id": "51c663602b4cc29fa7bca6a557f08ff5",
    "user": "Dhaval",
    "checkout_date": "2022-06-04"
}'
```

3. Fetch All Blocks (Fetch Chain)
```
curl --location --request GET 'localhost:3001'
```