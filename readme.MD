# API desenvolvida em C#

A ideia aqui é fazer um CRUD  usando C# e .NET tendo como cenário uma pizzaria que precisa de uma API capaz de lidar com o seu cadastro.

API criada com base no modelo disponível no .Net pelo comando `dotnet new webapi -f net6.0`.
Nela desenvolvi um controller que trabalha os métodos:

* `GET`- `{{URL}}:{{PORT}}/pizza`: listar todas as pizzas;
* `GET`- `{{URL}}:{{PORT}}/pizza/ID`: listar uma pizza específica;
* `POST`- `{{URL}}:{{PORT}}/pizza`: Criar uma pizza;
* `PUT`- `{{URL}}:{{PORT}}/pizza/ID`: alterar uma pizza;
* `DELETE`- `{{URL}}:{{PORT}}/pizza/ID`: deletar uma pizza;

## Como testar?
1. [Instalar o .NET Core 6.0] (https://dotnet.microsoft.com/en-us/download/dotnet/6.0);
2. Verificar se está tudo certo com a versão executando `dotnet --list-sdks`;
3. executar no terminal o comando `dotnet run`;

A API vai rodar em `https://localhost:7147`. Usando o Postman ou Insomnia faça as chamadas descritas acima. 
Os corpos para POST e PUT são os seguintes:

* `POST`:
```JSON
{
    "name": "Pepperoni",
    "isGlutenFree": false
}
```

* `PUT`:
```JSON
{
    "id": 3,
    "name": "Hawaiian",
    "isGlutenFree": false
}
```

