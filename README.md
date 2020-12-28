# API de Games
Minha primeira API desde 1997 kkkk
## Endpoints
### GET /games
Esse endpoint é responsável por retornar a listagem de todos os games cadastrados na BD.
#### Parametros
Nenhum
#### Respostas
##### OK! 200
Caso essa resposta aconteça você vai receber a listagem de todos os games.
Exemplo de  resposta:
```

[
    {
        "id": 1,
        "title": "Call of duty MW",
        "price": 201,
        "year": 2020
    },
    {
        "id": 2,
        "title": "Pro 2019",
        "price": 60,
        "year": 2019
    },
    {
        "id": 3,
        "title": "Minecraft",
        "price": 40,
        "year": 2010
    }
]

```

##### Falha na autenticação! 401
Caso essa resposta aconteça, isso significa que aconteceu alguma falha durante o processo de autenticação da requisição. Motivos: Token inválido, Token expirado
Exemplo de resposta
```
{
    "err": "Token invalido!"
}
```


### POST /auth
Esse endpoint é responsável por retornar o processo de login
#### Parametros
email: E-mail do usuário cadastrado no sistema


password: Senha do usuário cadastrado no sistema, com aquele determinado e-mail

Exemplo:
```

{
 "email":"goncalves@gmail.com",
 "password":"123456"
 
}
```
#### Respostas
##### OK! 200
Caso essa resposta aconteça você vai receber o token JWT para conseguir acessar endpoints protegidos na API.
Exemplo de  resposta:
```
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwiZW1haWwiOiJnb25jYWx2ZXNAZ21haWwuY29tIiwiaWF0IjoxNjA5MTY5MzY3LCJleHAiOjE2MDkzNDIxNjd9.fflJsrpmgOkH8DNlG0dafrrbt3DadisaokSNrwIgEQU"
}

```

##### Falha na autenticação! 401
Caso essa resposta aconteça, isso significa que aconteceu alguma falha durante o processo de autenticação da requisição. Motivos: Sena ou E-mail errados
Exemplo de resposta
```
{ 
err: "Credenciais inválidas" 
}
```
