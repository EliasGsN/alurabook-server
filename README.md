# Projeto: Biblioteca Online - AluraBook-Serve - Back-end

Este projeto é o back-end da aplicação de livros com Node.js e Express. Ele fornece as APIs necessárias para o front-end gerenciar livros e favoritos.

## Tecnologias Utilizadas

- Node.js
- Express
- CORS

## Estrutura do Projeto

### Arquivos Principais

- `app.js`: Configuração principal do servidor Express.
- `rotas/livro.js`: Rotas e lógica para operações relacionadas a livros.
- `rotas/favoritos.js`: Rotas e lógica para operações relacionadas a livros favoritos.

### Código do Servidor

O código do servidor é o seguinte:

```javascript
const express = require('express');
const rotaLivro = require('./rotas/livro');
const rotaFavoritos = require('./rotas/favoritos');

const cors = require('cors');

const app = express();
app.use(express.json());
app.use(cors({ origin: '*' }));

app.use('/livros', rotaLivro);
app.use('/favoritos', rotaFavoritos);

const port = 8000;

app.listen(port, () => {
    console.log(`Server is running on port ${port}`);
});
```

## Como Executar o Projeto

### Pré-requisitos

- Node.js
- npm

### Passos para Executar

1. Navegue até o diretório do back-end:
   ```bash
   cd caminho/para/back-end
   ```
2. Instale as dependências:
   ```bash
   npm install
   ```
3. Inicie o servidor:
   ```bash
   npm start
   ```

## Rotas da API

### `/livros`

- **GET** `/livros`: Retorna a lista de livros.
- **POST** `/livros`: Adiciona um novo livro.
- **PUT** `/livros/:id`: Atualiza um livro existente.
- **DELETE** `/livros/:id`: Remove um livro.

### `/favoritos`

- **GET** `/favoritos`: Retorna a lista de livros favoritos.
- **POST** `/favoritos`: Adiciona um livro à lista de favoritos.
- **DELETE** `/favoritos/:id`: Remove um livro da lista de favoritos.

## TODO

- [ ] Implementar autenticação de usuário.
- [ ] Adicionar validação de dados nas rotas.
- [ ] Implementar testes unitários para as rotas.
- [ ] Documentar a API com Swagger.
- [ ] Adicionar suporte para conexão com banco de dados.

---

# Project: Online Library - Back-end

This project is the back-end for the book application built with Node.js and Express. It provides the APIs needed for the front-end to manage books and favorites.

## Technologies Used

- Node.js
- Express
- CORS

## Project Structure

### Main Files

- `app.js`: Main Express server configuration.
- `routes/book.js`: Routes and logic for book-related operations.
- `routes/favorites.js`: Routes and logic for favorite books operations.

### Server Code

The server code is as follows:

```javascript
const express = require('express');
const routeBook = require('./routes/book');
const routeFavorites = require('./routes/favorites');

const cors = require('cors');

const app = express();
app.use(express.json());
app.use(cors({ origin: '*' }));

app.use('/books', routeBook);
app.use('/favorites', routeFavorites);

const port = 8000;

app.listen(port, () => {
    console.log(`Server is running on port ${port}`);
});
```

## How to Run the Project

### Prerequisites

- Node.js
- npm

### Steps to Run

1. Navigate to the back-end directory:
   ```bash
   cd path/to/back-end
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the server:
   ```bash
   npm start
   ```

## API Routes

### `/books`

- **GET** `/books`: Returns the list of books.
- **POST** `/books`: Adds a new book.
- **PUT** `/books/:id`: Updates an existing book.
- **DELETE** `/books/:id`: Deletes a book.

### `/favorites`

- **GET** `/favorites`: Returns the list of favorite books.
- **POST** `/favorites`: Adds a book to favorites.
- **DELETE** `/favorites/:id`: Removes a book from favorites.

## TODO

- [ ] Implement user authentication.
- [ ] Add data validation to routes.
- [ ] Implement unit tests for routes.
- [ ] Document the API with Swagger.
- [ ] Add support for database connection.
```
