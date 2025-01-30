# Desafio Docker + MySQL + Node.js

Este projeto é uma aplicação Node.js utilizando MySQL como banco de dados e Docker Compose para orquestração dos serviços.

## 🛠 Tecnologias Utilizadas

- **Node.js** (v20)
- **MySQL** (v8)
- **Docker & Docker Compose**
- **Yarn** (Gerenciador de pacotes)

---

## 🚀 Como iniciar o projeto

### 📌 1. Clonar o repositório

```sh
git clone https://github.com/jocelitojr2/desafio-rocker-compose
cd desafio-rocker-compose
```

### 📌 2. Criar o arquivo `.env`

Crie um arquivo `.env` na raiz do projeto com as seguintes variáveis:

```ini
# Configuração do Banco de Dados
DB_NAME=meubanco
DB_USER=meuusuario
DB_PASSWORD=senha
APP_PORT=3000
```

### 📌 3. Construir e subir os containers

```sh
docker-compose up --build
```

Isso iniciará os serviços:

- **MySQL** na porta `3306`
- **API** na porta definida em `APP_PORT`

Para rodar em background, use:

```sh
docker-compose up -d --build
```

---

## 🔄 Comandos úteis

### 🐳 Verificar containers rodando

```sh
docker ps
```

### 📜 Ver logs da API

```sh
docker-compose logs -f api-desafio
```

### 💻 Acessar terminal dentro do container da API

```sh
docker-compose exec api-desafio sh
```

### 💾 Acessar o MySQL dentro do container

```sh
docker-compose exec mysql mysql -u$DB_USER -p$DB_PASSWORD $DB_NAME
```

### ❌ Parar e remover os containers

```sh
docker-compose down
```

---

## 📋 Estrutura do Projeto

```
📂 seu-repositorio
 ┣ 📂 src          # Código-fonte
 ┣ 📜 Dockerfile   # Configuração do Docker
 ┣ 📜 docker-compose.yml  # Configuração dos serviços
 ┣ 📜 package.json  # Dependências do projeto
 ┣ 📜 yarn.lock
 ┗ 📜 .env.example  # Exemplo do arquivo .env
```
