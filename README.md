# hiker-database-server
Servidor PostgreSQL 18 com Docker.

### Pré-requisitos
- [Docker](https://www.docker.com/) instalado

### Configuração

As variáveis de ambiente ficam no arquivo `.env` na raiz do projeto, crie-o baseado nas credenciais
do projeto

```env
POSTGRES_USER=seu_usuario
POSTGRES_PASSWORD=sua_senha
POSTGRES_DB=sua_db
POSTGRES_PORT=5432
CONTAINER_NAME=hiker-postgres
```

---

### 1. Start

```bash
docker compose up -d
```

### 2. Ver logs

```bash
docker compose logs -f
```

### 3. Parar

```bash
docker compose down
```

### 4. Conectar ao banco

```bash
docker exec -it hiker-postgres psql -U hiker_user -d hiker_db
```

### 5. Remover container e volume (apaga os dados)

```bash
docker compose down -v
```