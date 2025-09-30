# Weather-Ai-Agent
Questo repository contiene un workflow n8n che invia ogni mattina alle 6:00 un’email con l’aggiornamento meteo per quattro città italiane.  Lo scopo è tenere informati i membri della famiglia, che vivono in città diverse, così da sapere le condizioni meteo degli altri e sentirsi più tranquilli.

## ✨ Funzionalità
- Ogni giorno alle **6:00 AM** raccoglie i dati meteo aggiornati.  
- Prepara un’**email breve e cordiale** di buongiorno.  
- Per ogni città indica:
  - Condizione del cielo (soleggiato, nuvoloso, pioggia, ecc.)  
  - Temperature minima e massima  
- Aggiunge consigli pratici:
  - Se è probabile pioggia → ricordare di portare l’ombrello ☔  
  - Suggerire il tipo di giacca/abbigliamento (leggera, media, pesante)  

---

## 📧 Esempio di output

**Subject:** Good Morning – Today’s Weather Update  

**Body:**  
Good morning everyone,  
here’s today’s forecast:  

- Palermo: [condition], min [X]°C / max [Y]°C  
- Sciacca: [condition], min [X]°C / max [Y]°C  
- Verona: [condition], min [X]°C / max [Y]°C  
- Padova: [condition], min [X]°C / max [Y]°C  

Advice: Wear [type of jacket]. [Umbrella suggestion if needed].  

Have a great day! 🌞  

---

## 🚀 Come usare il workflow
1. Apri n8n.  
2. Vai su **Import → Upload from file**.  
3. Carica `ai_agent.json` da questo repository.  
4. Configura i tuoi nodi:
   - API key/metodo per recuperare i dati meteo  
   - Destinatari email  
5. Attiva il workflow: ogni mattina alle 6:00 riceverai il meteo aggiornato.  

---
