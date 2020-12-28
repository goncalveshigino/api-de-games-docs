# API de Games
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
