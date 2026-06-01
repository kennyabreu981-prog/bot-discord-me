# 🤖 Bot Discord - 1v1 & Tickets

Um bot Discord completo com sistema de filas 1v1 e gerenciamento de tickets de suporte.

## ✨ Funcionalidades

- ⚔️ **Sistema 1v1**: Filas de matchmaking (Normal e Infinito)
- 🎫 **Tickets de Suporte**: Sistema completo de tickets com assumir/sair/fechar
- 🔐 **Seguro**: Token protegido com variáveis de ambiente
- 📝 **Slash Commands**: Comandos modernos do Discord

## 🚀 Como Usar

### 1️⃣ Pré-requisitos
- Node.js 16+ instalado
- Um bot Discord criado em https://discord.com/developers/applications
- Git instalado

### 2️⃣ Instalação Local

```bash
# Clonar o repositório
git clone https://github.com/kennyabreu981-prog/bot-discord-me.git
cd bot-discord-me

# Instalar dependências
npm install

# Criar arquivo .env
cp .env.example .env
```

### 3️⃣ Configurar o Token

1. Abra `.env`
2. Adicione seu token do bot:
```
TOKEN=seu_token_aqui
```

3. Salve e execute:
```bash
npm start
```

## 🎫 Configurar IDs

No arquivo `index.js`, edite:

```javascript
const CARGO_PERMITIDO = "1510756522328592585"; // Seu ID de cargo
```

Para pegar IDs:
- Ative modo desenvolvedor no Discord (Configurações > Privacidade > Modo Desenvolvedor)
- Clique direito em cargos/canais e escolha "Copiar ID"

## 🌐 Hosting (Grátis)

### Railway (Recomendado) ⭐

1. Acesse https://railway.app
2. Clique em "New Project" > "Deploy from GitHub"
3. Conecte seu repositório GitHub
4. Adicione variáveis de ambiente:
   - `TOKEN`: seu token do bot
5. Deploy automático!

### Replit

1. Acesse https://replit.com
2. Clique em "Import from GitHub"
3. Cole: `https://github.com/kennyabreu981-prog/bot-discord-me`
4. Crie arquivo `.replit`:
```
run = "npm install && npm start"
```
5. Adicione `.env` com seu token
6. Run!

### DigitalOcean

1. Crie um Droplet (Ubuntu 22.04)
2. SSH e execute:

```bash
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt-get install -y nodejs git

git clone https://github.com/kennyabreu981-prog/bot-discord-me.git
cd bot-discord-me
npm install

# Criar .env com seu token
nano .env

# Usar PM2 para rodar 24/7
npm install -g pm2
pm2 start index.js --name "discord-bot"
pm2 startup
pm2 save
```

## 📋 Comandos do Bot

- `/1v1` - Abrir painel de filas 1v1
- `/ticket` - Abrir painel de criação de ticket

## 🛠️ Desenvolvimento

Para modo desenvolvimento com auto-reload:

```bash
npm run dev
```

## 📧 Suporte

Encontrou um bug? Abra uma issue no repositório!

---

**Desenvolvido com ❤️ por kennyabreu981-prog**
