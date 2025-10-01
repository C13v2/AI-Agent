🤖 AI Assistant – Telegram Gateway

Un assistente AI multi-funzione che riceve richieste via Telegram, le interpreta tramite ChatGPT e le indirizza a tre agenti specializzati:

📧 Email Agent → scrive e invia email tramite Gmail

📅 Calendar Agent → gestisce eventi in Google Calendar

🔎 Research Agent → effettua ricerche sul web e fornisce risposte aggiornate

In aggiunta, l’assistente utilizza uno Sheet di contatti (nome, email, numero di telefono) per completare automaticamente le azioni.

🚀 Funzionalità

Input: Messaggi da Telegram

Routing intelligente: L’AI capisce se la richiesta riguarda Email, Calendar o Ricerca

Sheet lookup: Ricava email/telefono dal foglio contatti

Output:

Risposta breve e chiara su Telegram

Azione eseguita su Gmail, Google Calendar o Web Search

🛠️ Architettura

Telegram Bot → Riceve i messaggi degli utenti

Orchestrator Agent (ChatGPT) → Identifica l’intento:

[EMAIL] → passa al Email Agent

[CALENDAR] → passa al Calendar Agent

[RESEARCH] → passa al Research Agent

Email Agent → Genera subject/body e invia con Gmail

Calendar Agent → Crea/aggiorna/cancella eventi in Google Calendar

Research Agent → Fa ricerca sul web e sintetizza le informazioni

⚙️ Setup

Clona il repository

git clone https://github.com/tuo-username/ai-assistant-telegram.git
cd ai-assistant-telegram


Configura i servizi esterni

Crea un bot Telegram tramite BotFather

Abilita Gmail API e Google Calendar API

Prepara un Google Sheet con colonne: Name | Email | Phone

Imposta le variabili ambiente

TELEGRAM_BOT_TOKEN=xxx
OPENAI_API_KEY=xxx
GOOGLE_SHEETS_ID=xxx
GMAIL_CREDENTIALS=xxx
CALENDAR_CREDENTIALS=xxx


Configura i workflow (puoi usare n8n, Zapier, Make o altro sistema di automazione)

Trigger Telegram → Orchestrator Agent

Routing verso Email / Calendar / Research Agents

Output su Gmail / Google Calendar / Web Search

Risposta finale → Telegram

Google Sheet → Database dei contatti per email e numeri

Telegram Bot → Invia la conferma o la risposta finale all’utente
