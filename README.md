# AllBooks

Welcome to the AllBooks API!

AllBooks is an online store that sells books from Casa do Código.  
It is an MVP that is just getting started and still has many new features to be developed.

# JSONServer + JWT Auth

This is a mocked REST API, using json-server and JWT.

## 🛠️ Installation

```bash
$ npm install
$ npm run start-auth
```

## 🛠️ How to register?

You can do this by making a POST request to:

```
POST http://localhost:8000/public/registrar
```

With the following data:

```
{
    "nome": "vinicios neves",
    "email": "vinicios@alura.com.br",
    "senha": "123456",
    "endereco": "Rua Vergueiro, 3185",
    "complemento": "Vila Mariana",
    "cep": "04101-300"
}
```

Note that the email is a unique field and users with duplicate emails will not be saved.

## 🛠️ How to log in?

You can do this by making a POST request to:

```
POST http://localhost:8000/public/login
```

With the following data:

```
{
  "email": "vinicios@alura.com.br",
  "senha": "123456"
}
```

You will receive a token in the following format:

```
{
   "access_token": "<ACCESS_TOKEN>",
   "user": { ... user data ... }
}
```

## Authenticate subsequent requests?

Then, add this same token to the headers of the next requests:

```
Authorization: Bearer <ACCESS_TOKEN>
```