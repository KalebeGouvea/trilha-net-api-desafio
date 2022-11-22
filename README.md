# API - Gerenciador de tarefas
### Descrição do projeto

O projeto é um fork de um desafio do módulo de API e Entity Framework da [DIO][DIO] onde foram usados os conhecimentos adquiridos no curso para dar continuidade ao código disponibilizado pela metade.
A Web API consiste de um sistema gerenciador de tarefas utilizando CRUD, onde é possível cadastrar uma lista de tarefas que permitirá organizar melhor uma rotina.

### Endpoints:

| Verbo  | Endpoint                | Parâmetro | Body          |
|--------|-------------------------|-----------|---------------|
| GET    | /Tarefa/{id}            | id        | N/A           |
| PUT    | /Tarefa/{id}            | id        | Schema Tarefa |
| DELETE | /Tarefa/{id}            | id        | N/A           |
| GET    | /Tarefa/ObterTodos      | N/A       | N/A           |
| GET    | /Tarefa/ObterPorTitulo  | titulo    | N/A           |
| GET    | /Tarefa/ObterPorData    | data      | N/A           |
| GET    | /Tarefa/ObterPorStatus  | status    | N/A           |
| POST   | /Tarefa                 | N/A       | Schema Tarefa |

### Schema:
Esse é o schema (model) de Tarefa, utilizado para passar para os métodos que exigirem

```json
{
  "id": 0,
  "titulo": "string",
  "descricao": "string",
  "data": "2022-06-08T01:31:07.056Z",
  "status": "Pendente"
}
```

### Swagger:
A documentação da API (Swagger) também pode ser acessada no seguinte endereço, utilizando a porta definida:
https://localhost:PORT/swagger

![Métodos Swagger](swagger.png)

### Requisitos para rodar:
- .NET 6.0
- Entity Framework Core
- SQL Server 2019

### Como rodar:
Instale o .NET 6.0 SDK diretamente da página da Microsoft:
```
https://dotnet.microsoft.com/en-us/download/dotnet/6.0
```
Instale o Entity Framework Core pelo CLI do .NET no terminal:
```
dotnet tool install --global dotnet-ef
```
Com o SQL Server 2019 instalado e rodando, a Autenticação do Windows precisa estar habilitada e o nome do servidor precisa estar definido conforme abaixo:
```
localhost\sqlexpress
```
Caso contrário, a conexão precisa ser alterada no arquivo appsettings.Development.json

No terminal, clone o projeto:
```
git clone https://github.com/KalebeGouvea/tarefas-app.git
```
Acesse a pasta do projeto, rode o seguinte comando e o projeto deve ser aberto no navegador em seguida:
```
dotnet watch run
```

[DIO]: http://www.dio.me "DIO"
