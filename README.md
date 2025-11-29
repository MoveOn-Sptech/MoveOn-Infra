# 📦 MoveOn Infra

Repositório de configuração da infraestrutura do projeto acadêmico **MoveOn**.  
Aqui você encontra os arquivos necessários para subir o ambiente utilizando **Docker Compose**.

---

## 🚀 Como utilizar

### 1. Clonar o repositório
```bash
git clone https://github.com/MoveOn-Sptech/MoveOn-Infra.git
```

### 2. Entrar no diretório
```bash
cd MoveOn-Infra
```

### 3. Criar o arquivo `.env`
Crie um arquivo `.env` na raiz do projeto, seguindo o modelo disponível em `.env.example`:

```bash
nano .env
```

Exemplo de configuração:
```env
APP_PORT=
APP_HOST=
AMBIENTE_PROCESSO=

# DATABASE 

DB_HOST=
DB_DATABASE=
DB_USER=
DB_PASSWORD=
DB_PORT=

# Credenciais de usuario aws

AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_SESSION_TOKEN=

# Credenciais de bucket s3 da base de dados
AWS_BUCKET_NAME=
AWS_BUCKET_KEY_OBJECT=

# Credencias do SLACK
SLACK_BOT_TOKEN=
```

---

## 🐳 Instalar Docker e Docker Compose

Certifique-se de ter o **Docker** e o **Docker Compose** instalados.

### Atualizar pacotes
```bash
sudo apt update && sudo apt upgrade -y
```

### Instalar Docker

```bash
sudo apt install docker.io
sudo systemctl start docker
```

### Instalar Docker Compose

```bash
sudo curl -L "https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

### Verificar instalação
```bash
docker-compose version
```
```bash
docker -v
```
---

## ▶️ Rodar o projeto

Para subir os containers, execute:
```bash
sudo docker-compose up
```

---

## 📌 Observações
- Certifique-se de que as portas configuradas no `.env` não estejam em uso por outros serviços.
- Caso queira rodar em segundo plano, utilize:
  ```bash
  sudo docker-compose up -d --build
  ```
- Para parar os containers:
  ```bash
  sudo docker-compose down -v
  ```
