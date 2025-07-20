# a2syncode - Ambiente Docker para Desenvolvimento

Este repositório foi criado pela **a2syncode** para facilitar o desenvolvimento de aplicações modernas, fornecendo ambientes prontos para MongoDB, PostgreSQL, Redis e Portainer, todos orquestrados via Docker Compose.

## Serviços Disponíveis
- **MongoDB + Mongo Express**
- **PostgreSQL + pgAdmin**
- **Redis + Redis Commander**
- **Portainer** (gerenciamento visual de containers)

## Como usar

### 1. Clone o repositório
```bash
git clone <repo-url>
cd .docker-images
```

### 2. Configure as variáveis de ambiente
Copie o arquivo `env.example` para `.env` e ajuste os valores conforme sua necessidade:
```bash
cp env.example .env
```

### 3. Suba o serviço desejado
Cada serviço está em sua própria pasta. Para subir, por exemplo, o MongoDB:
```bash
cd mongo
docker-compose --env-file ../.env up -d
```
Repita para os outros serviços (`postgresql`, `redis`, `01-portainer`).

### 4. Acesse as interfaces web
- **Mongo Express:** http://localhost:${MONGO_EXPRESS_PORT}
- **pgAdmin:** http://localhost:${PGADMIN_PORT}
- **Redis Commander:** http://localhost:${REDIS_COMMANDER_PORT}
- **Portainer:** http://localhost:${PORTAINER_PORT}

> As portas podem ser alteradas no arquivo `.env`.

## Recomendações
- Nunca versionar o arquivo `.env` com senhas reais.
- Altere as senhas padrão antes de usar em produção.
- Use o Portainer para facilitar o gerenciamento dos containers.

---

Feito com ❤️ pela equipe **a2syncode** para acelerar seu desenvolvimento! 