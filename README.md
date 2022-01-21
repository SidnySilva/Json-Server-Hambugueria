## **Endpoints**

`GET /users - FORMATO DA RESPOSTA - STATUS 200`

```json
[
  {
    "email": "sid@sid.com",
    "password": "$2a$10$LeydfwAcq.TjxCaZTDI/r..B8hCf0OqPhjxLC0ZL1MaCpDc0aVgXO",
    "name": "sid",
    "id": 10
  }
]
```

`POST /users - `
` FORMATO DA RESPOSTA - STATUS 400`

```json
{
  "status": "error",
  "message": ["email", "password is required"]
}
```

Email já cadastrado:

`POST /users - `
` FORMATO DA RESPOSTA - STATUS 400`

```json
{
  "status": "error",
  "message": "Email already exists"
}
```

<h2 align = "center"> Login </h2>

`POST /login - FORMATO DA REQUISIÇÃO`

```json
{
  "email": "johndoe@email.com",
  "password": "123456"
}
```

Caso dê tudo certo, a resposta será assim:

`POST /users - FORMATO DA RESPOSTA - STATUS 201`

```json
{
  "user": {
    "email": "sid@sid.com",
    "password": "$2a$10$LeydfwAcq.TjxCaZTDI/r..B8hCf0OqPhjxLC0ZL1MaCpDc0aVgXO",
    "name": "sid",
    "id": 10
  },
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpYXQiOjE2MDcxODM3NzYsImV4cCI6MTYwNzQ0Mjk3Niwic3ViIjoiMmE3NWUxMmQtZmQxYy00ODFkLWJhODgtNGQ4YjE3MTAzYjJhIn0.UY67X23mPYAAzT43uFWZDHPUakd2STo5w4AuOcppkyQ"
}
```

`POST /products - FORMATO DA RESPOSTA - STATUS 201`

```json
{
  "products": {
    "id": 1,
    "name": "Hamburguer",
    "category": "Sanduíches",
    "price": 14,
    "img": "https://i.ibb.co/fpVHnZL/hamburguer.png"
}
```
