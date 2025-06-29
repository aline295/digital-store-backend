# 🛍️ Digital Store - Backend

API RESTful para gerenciar um e-commerce digital. Desenvolvida com Node.js, Express e Sequelize (PostgreSQL), com autenticação via JWT.

---

## 🚀 Tecnologias utilizadas

- [Node.js](https://nodejs.org/)
- [Express](https://expressjs.com/)
- [Sequelize](https://sequelize.org/)
- [PostgreSQL](https://www.postgresql.org/)
- [JWT (jsonwebtoken)](https://github.com/auth0/node-jsonwebtoken)
- [bcryptjs](https://github.com/dcodeIO/bcrypt.js)
- [dotenv](https://github.com/motdotla/dotenv)
- [Jest](https://jestjs.io/)
- [Supertest](https://github.com/visionmedia/supertest)
- [Nodemon](https://nodemon.io/)

---

## 📁 Estrutura do projeto

```
src/
├── app.js               # Configuração do Express
├── server.js            # Inicialização do servidor
├── controllers/         # Controladores (User, Auth)
├── middleware/          # Middlewares de autenticação
├── routes/              # Arquivos de rotas
├── database/
│   ├── index.js         # Conexão com Sequelize
│   ├── models/          # Models do Sequelize
│   └── migrations/      # Migrations do banco
└── config/
    └── auth.js          # Configuração do JWT
```

---

## ⚙️ Instalação e execução

### 1. Clone o repositório

```bash
git clone https://github.com/aline295/digital-store-backend.git
cd digital-store-backend
```

### 2. Instale as dependências

```bash
npm install
```

### 3. Configure as variáveis de ambiente

Crie um arquivo `.env` na raiz com o seguinte conteúdo:

```env
PORT=3001
DB_NAME=seu_banco
DB_USER=seu_usuario
DB_PASS=sua_senha
DB_HOST=localhost
JWT_SECRET=sua_chave_jwt
```

### 4. Execute as migrations

```bash
npx sequelize-cli db:migrate
```

### 5. Inicie o servidor

```bash
npm run dev
```

O servidor será iniciado em: [http://localhost:3001](http://localhost:3001)

---

## 🔐 Autenticação

A autenticação é feita via JWT. Após autenticar-se, o token deve ser enviado no header:

```http
Authorization: Bearer <token>
```

---

## 📚 Principais rotas

| Método | Rota         | Descrição                            | Protegida |
|--------|--------------|--------------------------------------|-----------|
| POST   | `/token`     | Gera token de autenticação           | ❌        |
| POST   | `/users`     | Cria um novo usuário                 | ❌        |
| GET    | `/users/:id` | Retorna informações de um usuário    | ❌        |
| PUT    | `/users/:id` | Atualiza dados de um usuário         | ✅        |
| DELETE | `/users/:id` | Remove um usuário                    | ✅        |

---

## 🧪 Testes

Execute os testes com:

```bash
npm test
```

---

## 🧠 Requisitos

- Node.js v18 ou superior
- PostgreSQL instalado e em execução
- Sequelize CLI instalado globalmente (opcional):  
  ```bash
  npm install -g sequelize-cli
  ```

---

## 📝 Licença

Este projeto está licenciado sob os termos da licença ISC.

---

Desenvolvido com 💙 por [@aline295](https://github.com/aline295)
