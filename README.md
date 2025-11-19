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
```

---

## 🐳 Instalar Docker Compose

Certifique-se de ter o **Docker** e o **Docker Compose** instalados.

### Atualizar pacotes
```bash
sudo apt update && sudo apt upgrade -y
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

---

## ▶️ Rodar o projeto

Para subir os containers, execute:
```bash
docker compose up
```

---

## 📌 Observações
- Certifique-se de que as portas configuradas no `.env` não estejam em uso por outros serviços.
- Caso queira rodar em segundo plano, utilize:
  ```bash
  docker compose up -d --build
  ```
- Para parar os containers:
  ```bash
  docker compose down -v
  ```
