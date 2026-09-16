# Sistema de Cadastro de Alunos
Projeto acadêmico desenvolvido para demonstrar a criação de um sistema de cadastro de alunos com PHP, MySQL e MySQLi. O objetivo principal é praticar operações de CRUD, validação de dados e segurança no backend.

## 📌 Sobre o projeto

Este sistema permite:

- Cadastrar alunos
- Listar todos os registros
- Editar informações dos alunos
- Excluir alunos
- Validar campos obrigatórios e e-mails
- Aplicar medidas de segurança com Prepared Statements

## 🛠️ Tecnologias utilizadas

- PHP
- MySQL
- MySQLi
- HTML5
- CSS3
- XAMPP
- phpMyAdmin

## 🧩 Estrutura do projeto

```text
sistema-alunos/
├── index.php
├── cadastrar.php
├── listar.php
├── editar.php
├── excluir.php
├── conexao.php
├── style.css
├── banco.sql
├── README.md
└── LICENSE (opcional)
```

## 🚀 Como executar

### 1. Preparar o ambiente

Instale o [XAMPP](https://www.apachefriends.org/) e inicie os serviços:

- Apache
- MySQL

### 2. Copiar o projeto

Coloque a pasta do projeto dentro do diretório do XAMPP:

```text
C:\xampp\htdocs\sistema-alunos
```

### 3. Criar o banco de dados

Acesse o phpMyAdmin em:

```text
http://localhost/phpmyadmin
```

Importe o arquivo `banco.sql`.

### 4. Acessar a aplicação

Abra no navegador:

```text
http://localhost/sistema-alunos/
```

## 🗃️ Banco de dados

O script `banco.sql` cria o banco `escola_db` e a tabela `alunos` com os campos:

```sql
id INT AUTO_INCREMENT PRIMARY KEY,
nome VARCHAR(100) NOT NULL,
email VARCHAR(150) NOT NULL UNIQUE,
curso VARCHAR(100) NOT NULL
```

## 🔐 Segurança aplicada

O projeto utiliza boas práticas como:

- Prepared Statements
- Validação de dados no servidor
- Uso de `htmlspecialchars()` na saída HTML
- Verificação de e-mail duplicado
- Acesso seguro a consultas SQL

## 📸 Funcionalidades principais

### Cadastro
- Recebe nome, e-mail e curso
- Valida campos vazios
- Verifica e-mail válido
- Evita duplicidade

### Listagem
- Exibe todos os alunos cadastrados em tabela

### Edição
- Permite alterar nome e curso
- Mantém o e-mail como dado principal de identificação

### Exclusão
- Remove o aluno com confirmação antes da exclusão

## ✅ Conclusão

Este projeto foi desenvolvido como uma aplicação simples, didática e funcional para demonstrar o funcionamento de um CRUD em PHP com banco de dados MySQL. Ele é ideal para estudo, apresentação acadêmica e aprofundamento em desenvolvimento web.

---

Desenvolvido para fins acadêmicos e de aprendizagem.


### 8. Teste contra SQL Injection

No campo de nome ou e-mail, teste o valor:

```text
' OR 1=1 --
```

O sistema deverá tratar o conteúdo como texto. A consulta não deverá ser alterada e nenhum registro indevido deverá ser retornado ou excluído.

## Diagnóstico de erros

Durante o desenvolvimento, funções como estas podem ajudar a identificar problemas:

```php
mysqli_connect_error();
mysqli_error($conexao);
```

Neste exercício, as mensagens detalhadas do banco não são exibidas para o usuário final, pois podem revelar informações internas da aplicação.

## O que este exercício demonstra

Este projeto demonstra:

- Validação de dados no servidor.
- Uso de `$_POST` para receber formulários.
- Uso de `$_GET` para identificar registros.
- Uso de `trim()` para remover espaços extras.
- Uso de `filter_var()` para validar e-mails.
- Uso de `htmlspecialchars()` para tornar a saída HTML mais segura.
- Uso de `mysqli_connect()` para conexão.
- Uso de `mysqli_prepare()` para preparar consultas.
- Uso de `mysqli_stmt_bind_param()` para vincular parâmetros.
- Uso de `mysqli_stmt_execute()` para executar consultas.
- Operações `INSERT`, `SELECT`, `UPDATE` e `DELETE`.
- Implementação das quatro operações do CRUD.
- Proteção contra SQL Injection.
- Restrição de e-mail duplicado com `UNIQUE`.

</div>
