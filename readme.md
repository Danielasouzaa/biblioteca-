# Sistema de Gerenciamento de Biblioteca

Este projeto implementa um banco de dados para gerenciamento de uma biblioteca, incluindo tabelas para autores, livros e empréstimos de livros. Ele utiliza comandos SQL para criar e manipular os dados, oferecendo funcionalidades como inserção de autores e livros, registro de empréstimos, consultas de dados e operações de atualização e exclusão.

## Estrutura do Banco de Dados

O banco de dados contém as seguintes tabelas:

1. **Autores**: Armazena informações sobre os autores.
   - `AutorID`: Identificador único do autor (chave primária).
   - `Nome`: Nome do autor.
   - `Nacionalidade`: País de origem do autor.

2. **Livros**: Armazena informações sobre os livros.
   - `LivroID`: Identificador único do livro (chave primária).
   - `Titulo`: Título do livro.
   - `AutorID`: Referência ao autor do livro (chave estrangeira para a tabela `Autores`).
   - `AnoPublicacao`: Ano em que o livro foi publicado.
   - `Genero`: Gênero literário do livro.

3. **Empréstimos**: Registra os empréstimos de livros.
   - `EmprestimoID`: Identificador único do empréstimo (chave primária).
   - `LivroID`: Referência ao livro emprestado (chave estrangeira para a tabela `Livros`).
   - `DataEmprestimo`: Data em que o livro foi emprestado.
   - `DataDevolucao`: Data de devolução do livro (pode ser nula se o livro ainda não foi devolvido).
   - `NomeUsuario`: Nome do usuário que pegou o livro emprestado.

## Passos para Execução

1. **Criação do Banco de Dados**:
   Execute os comandos SQL a partir do **Passo 1** para criar o banco de dados `Biblioteca` e as tabelas necessárias.

2. **Inserção de Dados**:
   Use os comandos a partir do **Passo 5** para inserir registros nas tabelas de `Autores`, `Livros` e `Emprestimos`.

3. **Consultas**:
   - Liste todos os livros com os nomes dos autores.
   - Consulte os empréstimos que ainda estão em aberto (sem data de devolução).

4. **Atualização e Exclusão**:
   - Atualize a data de devolução de um empréstimo específico.
   - Remova um livro e seus empréstimos associados do banco de dados.

## Comandos SQL

### Criação de Tabelas

- A tabela `Autores` é criada com um identificador único para cada autor.
- A tabela `Livros` armazena informações sobre os livros e inclui uma chave estrangeira para a tabela `Autores`.
- A tabela `Emprestimos` registra os empréstimos, incluindo a data de empréstimo e a data de devolução, além do nome do usuário.

### Inserção de Dados

- Inserção de exemplos de autores, livros e empréstimos com o comando `INSERT INTO`.

### Consultas

- Consultas SQL para listar os livros com seus autores e os empréstimos em aberto.

### Atualização de Dados

- Atualização da data de devolução de um empréstimo.

### Exclusão de Dados

- Exclusão de registros de empréstimos e remoção de um livro específico do banco de dados.

## Requisitos

- **MySQL** ou outro sistema de gerenciamento de banco de dados compatível com SQL.

## Estrutura do Projeto

- `create_database.sql`: Contém os comandos SQL necessários para criar as tabelas e inserir os dados.
- `queries.sql`: Contém as consultas SQL e operações de atualização/exclusão.

## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para sugerir melhorias ou abrir um Pull Request no repositório.

## Licença

Este projeto está sob a licença MIT.
