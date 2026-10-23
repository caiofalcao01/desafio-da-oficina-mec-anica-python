# 🚗 Sistema de Gerenciamento de Oficina Mecânica

Sistema web para gestão e controle de oficinas mecânicas, desenvolvido em **Python (Flask)** e **MySQL**. A aplicação permite gerenciar clientes, veículos, agendamentos de serviços e controle de acesso com autenticação de usuários.

---

## 🚀 Funcionalidades

- **🔐 Autenticação e Controle de Acesso:** Login seguro para usuários cadastrados no sistema.
- **👤 Gestão de Clientes:** Cadastro, listagem e atualização de informações dos clientes da oficina.
- **🚘 Gestão de Veículos:** Associação de veículos aos seus respectivos proprietários (clientes).
- **📅 Agendamento de Serviços:** Marcação e acompanhamento de horários e serviços para os veículos.
- **📊 Painel Principal:** Interface unificada para navegação entre os módulos do sistema.

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Função no Projeto |
| :--- | :--- |
| **Python** | Linguagem backend principal |
| **Flask** | Microframework para rotas e regras de negócio |
| **MySQL / MariaDB** | Banco de dados relacional (`saep_db.sql`) |
| **HTML5 / CSS3** | Estruturação e estilização da interface web |
| **JavaScript (ES6+)** | Interatividade no frontend (`app.js`) |
| **Jinja2** | Motor de templates para renderização dinâmica das páginas |

---

## 🗄️ Banco de Dados

O projeto utiliza um banco de dados relacional. O script SQL com a estrutura das tabelas e dados iniciais está localizado no arquivo `saep_db.sql`.

### Como importar o banco de dados:
1. Abra seu gerenciador de banco de dados (ex: MySQL Workbench, phpMyAdmin ou via CLI).
2. Crie uma nova base de dados ou execute diretamente o arquivo `saep_db.sql`:
   ```sql
   SOURCE caminho/para/sistema_oficina/saep_db.sql;
   ```

---

## 📦 Observação sobre a pasta `__pycache__`

Arquivos `.pyc` dentro da pasta `__pycache__` são arquivos temporários compilados pelo Python. Recomenda-se adicionar essa pasta ao arquivo `.gitignore` para não enviá-la ao GitHub:

```text
__pycache__/
*.pyc
```

---

## 🛠️ Como Baixar e Executar o Projeto

Siga os passos abaixo para configurar e executar o sistema no seu ambiente local:

### 1. Pré-requisitos
Certifique-se de ter instalado em sua máquina:
- [Python 3.10+](https://www.python.org/)
- Servidor [MySQL](https://www.mysql.com/) ou [XAMPP](https://www.apachefriends.org/)

### 2. Clonar ou baixar o projeto
Baixe os arquivos do projeto e navegue até a pasta do sistema:
```bash
cd sistema_oficina
```

### 3. Criar e ativar um ambiente virtual (opcional, mas recomendado)
```bash
# Windows
python -m venv venv
.\venv\Scripts\activate

# Linux / macOS
python3 -m venv venv
source venv/bin/activate
```

### 4. Instalar as dependências
Instale todos os pacotes necessários listados no arquivo `requirements.txt`:
```bash
pip install -r requirements.txt
```

### 5. Configurar as credenciais do banco de dados
Verifique no arquivo `db.py` se os dados de conexão (host, usuário, senha e nome do banco) correspondem à sua configuração local do MySQL.

### 6. Testar a conexão com o banco
Antes de iniciar a aplicação, você pode validar a conexão executando:
```bash
python testar_conexao.py
```

### 7. Executar a aplicação
Inicie o servidor do Flask rodando o arquivo principal:
```bash
python app.py
```

Abra o seu navegador e acesse:
```text
http://127.0.0.1:5000
```

---

## 📁 Estrutura de Pastas

```text
sistema_oficina/
├── __pycache__/           # Arquivos de bytecode gerados pelo Python
├── static/                # Arquivos estáticos (CSS e JS)
│   ├── app.js             # Scripts de interatividade do frontend
│   └── style.css          # Estilização visual da aplicação
├── templates/             # Páginas HTML (Templates Jinja2)
│   ├── agendamentos.html  # Tela de gestão de agendamentos
│   ├── clientes.html      # Tela de gestão de clientes
│   ├── login.html         # Tela de autenticação
│   ├── principal.html     # Dashboard / Menu principal
│   └── veiculos.html      # Tela de gestão de veículos
├── agendamento.py         # Módulo de lógica de agendamentos
├── app.py                 # Ponto de entrada (Entrypoint) da aplicação Flask
├── autenticacao.py        # Módulo de lógica de login e sessões
├── clientes.py            # Módulo de lógica de clientes
├── db.py                  # Conexão e ajudantes de banco de dados
├── requirements.txt       # Lista de dependências do Python
├── rotas.py               # Definições de rotas do sistema
├── saep_db.sql            # Script do banco de dados MySQL
├── testar_conexao.py      # Script de teste de banco de dados
└── veiculos.py            # Módulo de lógica de veículos
```
