# 📚 Sistema de Gerenciamento de Biblioteca - BookShelter

Este é um sistema simples de gerenciamento de biblioteca feito em **C# com Entity Framework Core** e interface **console**, desenvolvido como projeto acadêmico para fins didáticos.

## 🎯 Objetivo

O sistema permite o gerenciamento de livros, usuários (alunos e professores) e empréstimos, com funcionalidades completas de cadastro, listagem, controle e relatórios.

## 🛠 Tecnologias Utilizadas

- C#
- .NET 6 ou superior
- Entity Framework Core
- SQLite (armazenamento local)
- LINQ
- Interface de console

---

## ✅ Funcionalidades

### 📗 Livros

- Cadastro de livros (título, autor, ano, ISBN)
- Listagem de livros
- Exclusão com validação de empréstimos ativos
- Verificação de quem está com o livro emprestado

### 👤 Usuários

- Cadastro de **Alunos** (nome, curso, matrícula)
- Cadastro de **Professores** (nome, departamento, registro)
- Listagem de todos os usuários com indicação se possuem livro emprestado
- Exclusão com verificação de livros ativos
- Identificação do livro em caso de exclusão bloqueada

### 🔄 Empréstimos

- Empréstimo de livros para usuários
- Validações:
  - Livro não pode ser emprestado se já estiver emprestado
  - Usuário só pode ter um livro emprestado por vez
- Devolução de livros
- Relatório com histórico de empréstimos (ativos e concluídos)

### 📊 Relatórios

- Relatório de todos os livros
- Relatório de todos os usuários com situação de empréstimos
- Histórico de todos os empréstimos com status e datas

---

## 💻 Como Executar

1. **Clone o repositório:**

```bash
git clone https://github.com/seu-usuario/sistema-biblioteca.git
cd sistema-biblioteca
```

2. **Abra o projeto no Visual Studio ou VS Code.**

3. **Restaure os pacotes e execute:**

Se estiver usando CLI:

```bash
dotnet restore
dotnet run
```

---

## 🧠 Estrutura do Projeto

```
/Models
  - Livro.cs
  - Usuario.cs
  - Aluno.cs
  - Professor.cs
  - Emprestimo.cs

/BibliotecaContext.cs

/biblioteca.db

/Program.cs (funções principais e menus)
```

---

## 📌 Regras de Negócio

- Um usuário não pode pegar mais de um livro emprestado ao mesmo tempo.
- Um livro só pode estar com um usuário por vez.
- Usuários com empréstimos ativos não podem ser excluídos.
- Livros emprestados não podem ser excluídos sem devolução.
- O sistema mostra mensagens explicativas quando essas regras são violadas.

---

## 📝 Observações

- O sistema usa `EnsureCreated()` para criar o banco automaticamente na primeira execução.
- Ideal para projetos acadêmicos e aprendizagem de EF Core.
- Pode ser estendido com uma interface gráfica futuramente.

---

## 👨‍💻 Autor

Projeto desenvolvido por **Rafael Dourado**.

---

## 📃 Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
