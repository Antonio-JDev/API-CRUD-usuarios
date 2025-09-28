# Backend - API de Gerenciamento de Usuários

Backend desenvolvido em Node.js para gerenciamento de usuários, implementando uma API RESTful com Express.js e MongoDB, utilizando Prisma ORM para manipulação de dados.

## Tecnologias Utilizadas

- **Runtime**: Node.js
- **Framework**: Express.js
- **Banco de Dados**: MongoDB
- **ORM**: Prisma
- **Linguagem**: JavaScript (ES Modules)

## Estrutura do Projeto

- `API`: Diretório principal da API
  - `server.js`: Servidor principal
  - `routes/`: Rotas da API
  - `models/`: Modelos de dados
  - `config/`: Configuração do Prisma
  - `data/`: Dados de exemplo
- `prisma`: Diretório do Prisma
  - `schema.prisma`: Modelo de dados
  - `generate`: Geração de código do Prisma Client
- `package.json`: Arquivo de dependências
- `README.md`: Documento de descrição

## Sumário

- [Instalação](#instalação)
- [Configuração do Prisma](#configuração-do-prisma)
- [Uso](#uso)
- [Endpoints](#endpoints)
- [Contribuição](#contribuição)
- [Licença](#licença)

## Pré-requisitos

- Node.js (versão 14 ou superior)
- MongoDB
- NPM ou Yarn

## Instalação e Configuração

1. **Clone o repositório**
```bash
git clone https://github.com/Antonio-JDev/API-CRUD-usuarios.git
cd API-CRUD-usuarios
```

2. **Instale as dependências**
```bash
npm install
```

3. **Configure o Prisma CLI e o Prisma Client**
```bash
npm install prisma --save-dev
npm install @prisma/client
```

4. **Inicialize o Prisma (caso ainda não tenha o diretório `prisma`)**
```bash
npx prisma init
```

5. **Configure sua string de conexão do MongoDB no arquivo `.env`**
```
DATABASE_URL="mongodb+srv://usuario:senha@host/db"
```

6. **Gere o Prisma Client após configurar o modelo no arquivo `schema.prisma`**
```bash
npx prisma generate
```

## Uso

Inicie o servidor local:

```bash
npm start
```

A API estará disponível em `http://localhost:3000`.

## Endpoints

### POST /usuarios

Cria um novo usuário.

**Body:**
```json
{
  "email": "usuario@email.com",
  "name": "Nome do Usuário",
  "age": "25"
}
```

**Resposta:**
```json
{
  "id": "id_gerado",
  "email": "usuario@email.com",
  "name": "Nome do Usuário",
  "age": "25"
}
```

### GET /usuarios

Lista todos os usuários cadastrados.

**Resposta:**
```json
[
  {
    "id": "id_gerado",
    "email": "usuario@email.com",
    "name": "Nome do Usuário",
    "age": "25"
  }
]
```

## Contribuição

Contribuições são bem-vindas! Abra uma issue ou envie um pull request.

## Licença

Este projeto está com a licença livre.