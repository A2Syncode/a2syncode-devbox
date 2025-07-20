# 🚀 a2syncode - Ambiente Docker para Desenvolvimento

Bem-vindo ao repositório **a2syncode**! Aqui você encontra um ambiente completo e pronto para acelerar o desenvolvimento de aplicações modernas, com bancos de dados e ferramentas essenciais, tudo orquestrado via Docker Compose.

---

## 🧩 Serviços Disponíveis

- 🟢 **MongoDB** + Mongo Express
- 🟦 **PostgreSQL** + pgAdmin
- 🔴 **Redis** + Redis Commander
- 🛠️ **Portainer** (gerenciamento visual de containers)

---

## 📦 Como Usar

### 1️⃣ Clone o repositório
```bash
git clone <repo-url>
cd a2syncode-devbox
```

### 2️⃣ Configure as variáveis de ambiente
Copie o arquivo de exemplo e personalize conforme sua necessidade:
```bash
cp env.example .env
```

### 3️⃣ Suba o serviço desejado
Cada serviço está em sua própria pasta. Exemplo para MongoDB:
```bash
cd mongo
docker-compose --env-file ../.env up -d
```
Repita para os outros serviços (`postgresql`, `redis`, `01-portainer`).

### 4️⃣ Acesse as interfaces web
- 🌱 **Mongo Express:** [http://localhost:${MONGO_EXPRESS_PORT}](http://localhost:${MONGO_EXPRESS_PORT})
- 🐘 **pgAdmin:** [http://localhost:${PGADMIN_PORT}](http://localhost:${PGADMIN_PORT})
- ⚡ **Redis Commander:** [http://localhost:${REDIS_COMMANDER_PORT}](http://localhost:${REDIS_COMMANDER_PORT})
- 🛠️ **Portainer:** [http://localhost:${PORTAINER_PORT}](http://localhost:${PORTAINER_PORT})

> ⚠️ As portas podem ser alteradas no arquivo `.env`.

---

## 💡 Recomendações Importantes

- 🔒 **Nunca** versionar o arquivo `.env` com senhas reais.
- 🛡️ Altere as senhas padrão antes de usar em produção.
- 🖥️ Use o Portainer para facilitar o gerenciamento dos containers.

---

## 👩‍💻 Feito com ❤️ por a2syncode

Acelere seu desenvolvimento com praticidade, segurança e organização!

---

<p align="center">
  <img src="https://img.shields.io/badge/Feito%20por-a2syncode-6c63ff?style=for-the-badge" alt="a2syncode badge" />
</p> 