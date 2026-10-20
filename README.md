# CRUD Java — API de Produtos

API REST desenvolvida em Java com Spring Boot para realizar operações CRUD (Create, Read, Update e Delete) de produtos, utilizando PostgreSQL para persistência dos dados.

## 🚀 Tecnologias utilizadas

- Java 21
- Spring Boot
- Spring Data JPA
- PostgreSQL
- Flyway
- Gradle

## 📋 Funcionalidades

- Cadastrar produtos
- Listar produtos
- Buscar produtos
- Atualizar produtos
- Excluir produtos

*Observação: mantenha nesta lista apenas as funcionalidades implementadas no projeto.*

## ⚙️ Pré-requisitos

Antes de executar a aplicação, você precisa ter instalado:

- Java JDK 21
- PostgreSQL
- Git (opcional, para clonar o repositório)

## 🛠️ Como executar o projeto

### 1. Clone o repositório

```bash
git clone https://github.com/Gabriel-Vas-Silva/CrudAplicationJava.git
```

### 2. Acesse a pasta do projeto

```bash
cd CrudAplicationJava
```

### 3. Configure o banco de dados

Crie um banco de dados PostgreSQL chamado `product-api`.

Configure as credenciais de acesso no arquivo:

`src/main/resources/application.properties`

Verifique as configurações de URL, usuário e senha do banco antes de executar a aplicação.

### 4. Execute a aplicação

No Windows, utilize o terminal dentro da pasta do projeto:

```powershell
.\gradlew.bat bootRun
```

A aplicação será iniciada na porta `8080`, caso não haja outra configuração.

## 🔗 Endpoints da API

A rota principal da API é:
`http://localhost:8080/products`

Utilize o Insomnia ou outra ferramenta para testar as requisições HTTP.

| Método HTTP | Operação |
|---|---|
| GET | Consultar produtos |
| POST | Cadastrar produto |
| PUT | Atualizar produto |
| DELETE | Excluir produto |

*Os métodos e as rotas específicas devem corresponder ao que está implementado no controller.*

### Exemplo de cadastro

**POST** `/products`

```json
{
  "name": "Teclado Gamer",
  "price": 250
}
```

Envie o JSON no corpo da requisição com o tipo de conteúdo `application/json`.

## 🗄️ Banco de dados

A aplicação utiliza PostgreSQL para armazenar os produtos. O Flyway é utilizado para gerenciar as migrações do banco de dados.
