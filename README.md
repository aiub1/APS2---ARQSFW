# API RESTful - Sistema de Postagens

Esta é uma API construída com **Node.js**, **Express** e **MongoDB** para gerenciamento de usuários, autores e postagens. A API segue o padrão **MVC** e utiliza **JWT** para autenticação, **Swagger** para documentação e **DTOs** para segurança na troca de dados.

---

## Tecnologias Utilizadas

- **Node.js**: Ambiente de execução JavaScript
- **Express**: Framework para construção de APIs
- **MongoDB + Mongoose**: Banco de dados NoSQL e ODM
- **Swagger (OpenAPI)**: Documentação de API
- **JSON Web Token (JWT)**: Autenticação stateless
- **BcryptJS**: Hashing de senhas
- **dotenv**: Gerenciamento de variáveis de ambiente

---

## Estrutura de Pastas

- Node.js
- Express
- MongoDB + Mongoose
- Swagger (OpenAPI)
- JSON Web Token (JWT)
- BcryptJS
- dotenv

```
src/
├── config/ # Configurações do sistema
├── controllers/ # Lógica das requisições
├── dtos/ # Objetos de transferência de dados
├── middleware/ # Interceptores de requisição
├── models/ # Modelos de dados
├── repositories/ # Camada de acesso a dados
├── routes/ # Definição de rotas
├── services/ # Lógica de negócios
├── app.js # Configuração do Express
└── server.js # Ponto de entrada
```

---

## Instalação

1. Clone o repositório:
```bash
git clone https://github.com/aiub1/APS2---ARQSFW.git
cd sua-api
```

2. Instale as dependências:
```bash
npm install
```

3. Configure o .env:
```bash
DB_CONNECTION_STRING=mongodb+srv://usuario:senha@cluster.mongodb.net/nomedobanco
JWT_SECRET=sua_chave_secreta
```
---

## Como Rodar o Projeto

Ambiente de Desenvolvimento
```bash
npm run dev
```

A API estará disponível em: `http://localhost:3000`

---

## Autenticação

Use a rota:

```http
POST /auth/login
```

Exemplo de body:
```json
{
  "email": "usuario@email.com",
  "password": "123456"
}
```

A resposta será um token JWT:

```json
{
  "accessToken": "jwt.token.aqui"
}
```

Utilize este token como:

```
Authorization: Bearer jwt.token.aqui
```

---

## Documentação (Swagger)

Acesse a documentação completa em:

```
http://localhost:3000/api-docs
```

---

## Principais Endpoints

### Usuários
- `GET /users` – Lista todos os usuários
- `POST /users` – Registra um novo usuário
- `GET /users/:id` – Busca por ID
- `PUT /users/:id` – Atualiza usuário (protegido)
- `DELETE /users/:id` – Remove usuário (protegido)

### Autores
- `GET /authors` – Lista todos
- `POST /authors` – Cria novo
- `GET /authors/:id` – Busca por ID
- `PUT /authors/:id` – Atualiza
- `DELETE /authors/:id` – Remove
- `GET /authors/search/:name` – Busca por nome

### Posts
- `GET /posts` – Lista posts
- `POST /posts` – Cria post
- `GET /posts/:id` – Busca post
- `PUT /posts/:id` – Atualiza
- `DELETE /posts/:id` – Remove
- `GET /posts/search?keyword=termo` – Busca por palavra-chave

---

## Estrutura de Pastas

```
src/
├── config/
├── controllers/
├── dtos/
├── middleware/
├── models/
├── repositories/
├── routes/
├── services/
├── app.js
server.js
```

---

## Observação
Este projeto foi desenvolvido como demonstração de uma API RESTful completa, implementando boas práticas como:

Separação de responsabilidades (MVC)

Autenticação segura com JWT

Documentação automatizada

Validação de dados com DTOs

---

## Contribuindo

Faça um fork do projeto

```
Crie sua branch (git checkout -b feature/NovaFeature)

Commit suas alterações (git commit -m 'Adiciona NovaFeature')

Push para a branch (git push origin feature/NovaFeature)
```

Abra um Pull Request
