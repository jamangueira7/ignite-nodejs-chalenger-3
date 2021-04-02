<img alt="GoStack" src=".github/rocketseat.png" />

<p align="center">
  <a href="#rocket-tecnologias">Tecnologias</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-projeto">Projeto</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-como-rodar">Como rodar</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-Rotas">Rotas</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-como-contribuir">Como contribuir</a>&nbsp;&nbsp;&nbsp;
</p>

<br>


## Ignite Node.js - Segundo desafio

## 🚀 Tecnologias

Esse projeto foi desenvolvido com as seguintes tecnologias:

- [NodeJS](https://nodejs.org/en/) - 0.63.3
- [Yarn](https://yarnpkg.com/) - 1.22.4
- [Npm](https://www.npmjs.com/) - 6.14.5


## 💻 Projeto

API para cadastra usuario e fazer o CRUD de tarefas.

Descrição do desafio [GoStack](https://www.notion.so/Desafio-02-Trabalhando-com-middlewares-4f89bf538c2e4ee291382b92bdc36790)


Resolulção do teste.
<p align="center">
  <img alt="resolucao" src=".github/teste.PNG" width="100%">
</p>

## 🚀 Como Rodar

- Clone o projeto.
- Entre na pasta do projeto e rode "yarn install" (pode usar npm install de acordo com a sua configuração).
- "yarn test" para rodar os testes.
- yarn run dev para rodar o projeto (localhost:3333).

## 👩🏿‍💻 Rotas

- **`POST /users`**: Rota para cadastro de usuarios.

Enviar:
```
{
    "name": "João",
    "username": "joao"
}
```
Retorna:
```
{
    "id": "bc57f695-ae37-48cf-9401-d8aa1f4fd914",
    "name": "João",
    "username": "joao",
    "pro": false,
    "todos": []
}
```

- **`GET /users/:id`**: Rota para retornar o usuarios.

Retorna:
```
{
    "id": "bc57f695-ae37-48cf-9401-d8aa1f4fd914",
    "name": "João",
    "username": "joao",
    "pro": false,
    "todos": []
}
```

- **`PATCH /users/:id/pro`**: Rota para ativar plano pro do usuarios.

Retorna:
```
{
    "id": "bc57f695-ae37-48cf-9401-d8aa1f4fd914",
    "name": "João",
    "username": "joao",
    "pro": true,
    "todos": []
}
```


- **`POST /todos`**: Rota para cadastrar tarefas dos ususarios.

Enviar headers:
```
{
    "username": "joao"
}
```

Enviar:
```
{
    "title": "Sei la",
    "deadline": "2021-03-31"
}
```

Retorna:
```
{
    "id": "12c44b61-61f8-4ab8-9365-49f107f1796f",
    "title": "Sei la",
    "deadline": "2021-03-31T00:00:00.000Z",
    "done": false,
    "created_at": "2021-04-01T01:50:51.046Z"
}
```
- **`GET /todos`**: Rota para buscar todas as tarefas de um usuario.

Enviar headers:
```
{
    "username": "joao"
}
```

Retorna:
```
[
    {
        "id": "12c44b61-61f8-4ab8-9365-49f107f1796f",
        "title": "Sei la",
        "deadline": "2021-03-31T00:00:00.000Z",
        "done": false,
        "created_at": "2021-04-01T01:50:51.046Z"
    },
    {
        "id": "47d9dbfa-5095-4465-85c6-9cb513c9c720",
        "title": "Sei la 2",
        "deadline": "2021-03-31T00:00:00.000Z",
        "done": false,
        "created_at": "2021-04-01T01:51:34.911Z"
    },
    {
        "id": "db9f09c6-d788-492c-ab23-59ed99ef1340",
        "title": "Sei la 3",
        "deadline": "2021-03-31T00:00:00.000Z",
        "done": false,
        "created_at": "2021-04-01T01:51:38.452Z"
    }
]
```

- **`PUT /todos/:id`**: Rota para alterar uma tarefa de um ususario.+

Enviar headers:
```
{
    "username": "joao"
}
```

Enviar:
```
{
    "title": "Sei la alterado",
    "deadline": "2021-04-02"
}
```

Retorna:
```
{
    "id": "12c44b61-61f8-4ab8-9365-49f107f1796f",
    "title": "Sei la alterado",
    "deadline": "2021-04-02",
    "done": false,
    "created_at": "2021-04-01T01:50:51.046Z"
}
```

- **`PATCH /todos/:id/done`**: Rota para alterar o campo done de uma tarefa de um ususario.+

Enviar headers:
```
{
    "username": "joao"
}
```

Retorna:
```
{
    "id": "12c44b61-61f8-4ab8-9365-49f107f1796f",
    "title": "Sei la alterado",
    "deadline": "2021-04-02",
    "done": true,
    "created_at": "2021-04-01T01:50:51.046Z"
}
```

- **`DELETE /todos/:id`**: Rota para deletar uma tarefa de um ususario.+

Enviar headers:
```
{
    "username": "joao"
}
```

## 🤔 Como contribuir

- Faça um fork desse repositório;
- Cria uma branch com a sua feature: `git checkout -b minha-feature`;
- Faça commit das suas alterações: `git commit -m 'feat: Minha nova feature'`;
- Faça push para a sua branch: `git push origin minha-feature`.

Depois que o merge da sua pull request for feito, você pode deletar a sua branch.

## 📝 Licença

Esse projeto está sob a licença MIT.
