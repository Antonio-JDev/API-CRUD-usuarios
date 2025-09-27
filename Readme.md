# API de Usuários

Esta API foi desenvolvida para gerenciar usuários, permitindo criar, listar, editar e deletar registros. Utiliza Node.js, Express e Prisma ORM com banco de dados MongoDB.

## Sumário

- [Instalação](#instalação)
- [Configuração do Prisma](#configuração-do-prisma)
- [Uso](#uso)
- [Endpoints](#endpoints)
- [Contribuição](#contribuição)
- [Licença](#licença)

## Instalação

Clone o repositório e instale as dependências:

```bash
git clone https://github.com/seu-usuario/projeto-api.git
cd projeto-api/API
npm install
```

## Configuração do Prisma

1. Instale o Prisma CLI e o Prisma Client:

```bash
npm install prisma --save-dev
npm install @prisma/client
```

2. Inicialize o Prisma (caso ainda não tenha o diretório `prisma`):

```bash
npx prisma init
```

3. Configure sua string de conexão do MongoDB no arquivo `.env`:

```
DATABASE_URL="mongodb+srv://usuario:senha@host/db"
```

4. Gere o Prisma Client após configurar o modelo no arquivo `schema.prisma`:

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