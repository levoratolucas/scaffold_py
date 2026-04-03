# 🚀 Gerador de Projeto Python MVC com SQLite

## 📌 Visão Geral

Este projeto consiste em um **scaffold (gerador automático)** para criação de aplicações Python utilizando:

* Arquitetura **MVC (Model-View-Controller)**
* Banco de dados **SQLite**
* Estrutura modular e orientada a objetos

O objetivo é acelerar a criação de novos projetos já com uma base sólida, organizada e funcional.

---

## 🧱 Estrutura Gerada

Após executar o script, a seguinte estrutura é criada:

```
raiz/
│ main.py
│ banco.db (criado automaticamente na execução)
│
└── app/
    ├── model/
    │   └── user_model.py
    │
    ├── view/
    │   └── user_view.py
    │
    ├── controller/
    │   └── user_controller.py
    │
    └── bd/
        ├── conexao.py
        └── user_repository.py
```

---

## ⚙️ Funcionamento

O script `scaffold.py` realiza automaticamente:

1. Criação da estrutura de diretórios
2. Criação dos arquivos base
3. Implementação de:

   * Model (`User`)
   * Repository (acesso ao SQLite)
   * Controller (regras de negócio)
   * View (interface CLI)
4. Criação de um banco SQLite
5. Inserção de um usuário padrão
6. Execução pronta do sistema

---

## 👤 Usuário Padrão

Por padrão, o sistema já inicia com:

* **Nome:** Lucas Levorato
* **Idade:** 31
* **Sexo:** Masculino

---

## ▶️ Como Executar

### 1. Gerar o projeto

```
python scaffold.py
```

---

### 2. Executar o sistema

```
python main.py
```

---

## 🧪 Saída esperada

```
Bom dia Lucas Levorato! Idade: 31 Sexo: Masculino
```

---

## 🔄 Personalização via CLI

É possível sobrescrever o usuário padrão:

```
python scaffold.py Maria 22 Feminino
```

---

## 🧠 Arquitetura

### 📦 Model

Responsável pela representação dos dados:

```
User(nome, idade, sexo)
```

---

### 💾 Repository

Camada de acesso ao banco:

* Criação da tabela
* Inserção de dados
* Consulta de registros

---

### 🎮 Controller

Regras de negócio:

* Criação do usuário padrão
* Comunicação entre Model e Repository

---

### 🖥️ View

Responsável pela saída de dados no terminal:

* Exibição do usuário

---

### 🚀 Main

Ponto de entrada da aplicação:

* Inicializa controller e view
* Executa fluxo principal

---

## 🗄️ Banco de Dados

* Tipo: SQLite
* Arquivo: `banco.db`
* Tabela: `users`

### Estrutura:

```
id INTEGER PRIMARY KEY
nome TEXT
idade INTEGER
sexo TEXT
```

---

## 📦 Geração de Executável

Para transformar em `.exe`:

```
pip install pyinstaller
pyinstaller --onefile main.py
```

Arquivo gerado em:

```
dist/main.exe
```

---

## 🔥 Possíveis Evoluções

* CRUD completo (Update/Delete)
* Interface gráfica (Tkinter / PySide)
* API REST (Flask / FastAPI)
* Autenticação de usuários
* Múltiplos models automáticos
* CLI profissional (`mvc new projeto`)
* Empacotamento como biblioteca (`pip install`)

---

## 🎯 Objetivo

Este scaffold foi criado para:

* Padronizar projetos Python
* Reduzir tempo de setup
* Aplicar boas práticas (MVC + OO)
* Servir como base para sistemas maiores

---

## 👨‍💻 Autor

Projeto gerado automaticamente com scaffold personalizado.

---
