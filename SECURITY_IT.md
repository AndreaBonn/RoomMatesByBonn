# Politica di Sicurezza

> **🇮🇹 Italiano** | **[🇬🇧 Read in English](./SECURITY.md)**

---

## 🔒 Panoramica Sicurezza

La sicurezza è una priorità assoluta per RoomMate App. Questo documento delinea le nostre pratiche di sicurezza, le versioni supportate e come segnalare vulnerabilità.

**Link Rapidi:**
- [Versioni Supportate](#versioni-supportate)
- [Segnalare una Vulnerabilità](#segnalare-una-vulnerabilità)
- [Best Practice di Sicurezza](#best-practice-di-sicurezza)
- [Protezione Dati](#protezione-dati)
- [Sicurezza Terze Parti](#sicurezza-terze-parti)

---

## 📋 Versioni Supportate

Manteniamo attivamente e forniamo aggiornamenti di sicurezza per le seguenti versioni:

| Versione | Supportata        | Stato |
| -------- | ----------------- | ----- |
| 1.0.x    | ✅ Sì            | Attiva |
| < 1.0    | ❌ No            | Deprecata |

**Politica di Aggiornamento:**
- Le patch di sicurezza vengono rilasciate il prima possibile dopo la scoperta
- Gli utenti vengono notificati degli aggiornamenti di sicurezza critici tramite l'applicazione
- Raccomandiamo di utilizzare sempre l'ultima versione

---

## 🚨 Segnalare una Vulnerabilità

Prendiamo sul serio tutte le vulnerabilità di sicurezza. Se scopri un problema di sicurezza, segui queste linee guida:

### Come Segnalare

**NON** creare una issue pubblica su GitHub per vulnerabilità di sicurezza.

Invece, segnala i problemi di sicurezza privatamente:

1. **Email**: Invia i dettagli a `andreabonacci95@protonmail.com`
2. **Oggetto**: Usa "SECURITY: [Breve Descrizione]"
3. **Includi**:
   - Descrizione della vulnerabilità
   - Passi per riprodurre il problema
   - Valutazione del potenziale impatto
   - Correzione suggerita (se presente)
   - Le tue informazioni di contatto

### Cosa Aspettarsi

- **Conferma**: Entro 48 ore dalla tua segnalazione
- **Valutazione Iniziale**: Entro 5 giorni lavorativi
- **Aggiornamenti di Stato**: Aggiornamenti regolari sui progressi
- **Tempistiche di Risoluzione**: Variano in base alla gravità
  - Critica: 1-7 giorni
  - Alta: 7-14 giorni
  - Media: 14-30 giorni
  - Bassa: 30-90 giorni

### Divulgazione Responsabile

Seguiamo pratiche di divulgazione responsabile:

1. **Riservatezza**: Manteniamo riservata la tua segnalazione fino al deployment di una correzione
2. **Riconoscimento**: Riconosciamo i ricercatori di sicurezza (con permesso)
3. **Coordinamento**: Lavoriamo con te per comprendere e risolvere il problema
4. **Divulgazione Pubblica**: Solo dopo il deployment di una correzione e dopo che gli utenti hanno avuto tempo di aggiornare

### Bug Bounty

Attualmente non offriamo un programma formale di bug bounty. Tuttavia, apprezziamo profondamente i ricercatori di sicurezza che ci aiutano a migliorare la sicurezza dell'applicazione.

---

## 🛡️ Best Practice di Sicurezza

### Per gli Utenti

#### Sicurezza Account

✅ **FAI**:
- Usa una password forte e unica (minimo 8 caratteri con maiuscole, minuscole, numeri e simboli)
- Abilita l'autenticazione a due fattori quando disponibile
- Mantieni sicuro il tuo account email (viene usato per il recupero password)
- Disconnettiti dai dispositivi condivisi
- Rivedi regolarmente l'attività del tuo account

❌ **NON FARE**:
- Condividere la tua password con nessuno, inclusi i coinquilini
- Usare la stessa password su più servizi
- Salvare password in posizioni non sicure
- Lasciare il tuo account connesso su computer pubblici

#### Codici Invito Casa

✅ **FAI**:
- Condividi i codici invito solo con coinquilini fidati
- Rigenera i codici invito se compromessi
- Rimuovi i membri che non vivono più nella casa

❌ **NON FARE**:
- Pubblicare codici invito pubblicamente (social media, forum, ecc.)
- Condividere codici invito con persone che non conosci
- Riutilizzare vecchi codici invito

#### API Key (Funzionalità IA)

✅ **FAI**:
- Mantieni riservate le tue API key dei provider IA
- Usa l'opzione di storage locale per massima sicurezza
- Imposta limiti di utilizzo sui tuoi account provider IA
- Ruota regolarmente le tue API key
- Monitora l'utilizzo e la fatturazione del tuo provider IA

❌ **NON FARE**:
- Condividere le tue API key con altri
- Usare API key da fonti non affidabili
- Memorizzare API key in testo semplice fuori dall'applicazione
- Usare API key di produzione per test

#### Privacy Dati

✅ **FAI**:
- Rivedi quali dati condividi con i coinquilini
- Usa password forti per documenti sensibili
- Rivedi regolarmente i membri della casa
- Fai attenzione a cosa pubblichi negli annunci

❌ **NON FARE**:
- Condividere informazioni personali sensibili in annunci pubblici
- Caricare documenti riservati senza crittografia
- Concedere accesso admin a utenti non fidati

### Per gli Amministratori

#### Gestione Casa

✅ **FAI**:
- Controlla regolarmente i membri della casa
- Rimuovi prontamente coinquilini inattivi o ex
- Rivedi e approva attentamente le richieste di nuovi membri
- Mantieni aggiornate le informazioni di contatto
- Fai backup regolari di dati importanti (funzionalità di esportazione)

❌ **NON FARE**:
- Concedere privilegi admin inutilmente
- Lasciare ex coinquilini con accesso
- Ignorare attività sospette
- Condividere credenziali admin

#### Gestione Dati

✅ **FAI**:
- Esporta regolarmente dati finanziari importanti
- Rivedi lo storico spese per anomalie
- Conserva ricevute per spese significative
- Documenta decisioni importanti della casa

❌ **NON FARE**:
- Eliminare record importanti senza backup
- Ignorare discrepanze nei dati finanziari
- Condividere pubblicamente informazioni sensibili della casa

---

## 🔐 Protezione Dati

### Archiviazione Dati

**Firebase Firestore**:
- Tutti i dati sono crittografati in transito (HTTPS/TLS)
- I dati a riposo sono crittografati da Google Cloud Platform
- L'accesso al database è controllato dalle Regole di Sicurezza Firestore
- Replica multi-regione per affidabilità

**Storage Locale**:
- Cache PWA per funzionalità offline
- IndexedDB per persistenza dati locale
- Invalidazione automatica della cache
- Storage sicuro per API key (quando selezionata l'opzione locale)

### Controllo Accesso Dati

**Accesso Basato su Ruoli**:
- **Admin**: Accesso completo ai dati della casa, gestione membri
- **Membro**: Accesso ai dati condivisi, diritti di modifica limitati
- **Utente**: Accesso solo ai dati personali e alle case di appartenenza

**Regole di Sicurezza**:
- Le Regole di Sicurezza Firestore applicano il controllo accessi a livello database
- Gli utenti possono accedere solo ai dati delle case di cui sono membri
- I dati personali (API key, profilo) sono accessibili solo dal proprietario
- I dati NPC (membro virtuale) sono accessibili da tutti i membri della casa

### Conservazione Dati

- **Dati Attivi**: Conservati mentre usi l'applicazione
- **Account Eliminati**: I dati sono anonimizzati ma conservati per record storici
- **Case Inattive**: I dati sono conservati indefinitamente (controlli tu l'eliminazione)
- **Esportazioni**: Puoi esportare tutti i tuoi dati in qualsiasi momento

### Eliminazione Dati

Gli utenti possono:
- Eliminare il proprio account (i dati del profilo vengono rimossi)
- Lasciare case (l'appartenenza viene rimossa, i dati storici rimangono)
- Eliminare contenuti creati (spese, annunci, ecc.)

Gli admin possono:
- Rimuovere membri dalle case
- Eliminare dati della casa
- Esportare tutti i dati della casa prima dell'eliminazione

---

## 🔗 Sicurezza Terze Parti

### Firebase (Google)

- **Sicurezza**: Sicurezza di livello enterprise da Google Cloud Platform
- **Conformità**: Conforme SOC 2, ISO 27001, GDPR
- **Documentazione**: [Sicurezza Firebase](https://firebase.google.com/support/privacy)

### Provider IA

**OpenAI**:
- Le API key sono crittografate
- I dati non sono usati per training del modello (secondo termini API)
- [Sicurezza OpenAI](https://openai.com/security)

**Anthropic Claude**:
- Sicurezza di livello enterprise
- Impegni sulla privacy dei dati
- [Sicurezza Anthropic](https://www.anthropic.com/security)

**Google Gemini**:
- Standard di sicurezza Google Cloud
- [Sicurezza Google AI](https://ai.google/responsibility/safety-security/)

**Groq**:
- Inferenza veloce con sicurezza
- [Sicurezza Groq](https://groq.com/security/)

### Brevo (Servizio Email)

- **Sicurezza**: Certificato ISO 27001
- **Conformità**: Conforme GDPR
- **Documentazione**: [Sicurezza Brevo](https://www.brevo.com/it/legal/securitypolicy/)

### Dipendenze

- Aggiornamenti regolari delle dipendenze via npm
- Scansione automatizzata delle vulnerabilità
- Patch di sicurezza applicate prontamente
- Footprint minimo delle dipendenze

---

## 🔍 Funzionalità di Sicurezza

### Autenticazione

- **Firebase Authentication**: Autenticazione standard del settore
- **Requisiti Password**: Minimo 8 caratteri, requisiti di complessità
- **Gestione Sessioni**: Sessioni sicure basate su token
- **Reset Password**: Recupero password sicuro basato su email

### Autorizzazione

- **Regole di Sicurezza Firestore**: Controllo accessi a livello database
- **Controllo Accessi Basato su Ruoli (RBAC)**: Ruoli admin e membro
- **Permessi a Livello Risorsa**: Controllo accessi granulare
- **Validazione Automatica**: Validazione lato server di tutte le operazioni

### Trasmissione Dati

- **Solo HTTPS**: Tutte le comunicazioni crittografate con TLS 1.2+
- **Header Sicuri**: CSP, HSTS, X-Frame-Options configurati
- **Sicurezza API**: Autenticazione bearer token per tutte le chiamate API

### Sicurezza Applicazione

- **Validazione Input**: Tutti gli input utente validati e sanitizzati
- **Protezione XSS**: Protezione XSS integrata di React
- **Protezione CSRF**: Protezione CSRF basata su token
- **SQL Injection**: Non applicabile (database NoSQL)
- **Rate Limiting**: Protezione contro attacchi brute force

### Sicurezza PWA

- **Service Worker**: Strategie di caching sicure
- **HTTPS Richiesto**: PWA funziona solo su HTTPS
- **Content Security Policy**: Header CSP rigorosi
- **Subresource Integrity**: Risorse esterne verificate

---

## 📱 Sicurezza Mobile

### Installazione PWA

- Installa solo da fonti affidabili (URL ufficiale)
- Verifica la connessione HTTPS prima dell'installazione
- Rivedi i permessi richiesti dall'app

### Dati Offline

- I dati offline sono memorizzati in modo sicuro in IndexedDB
- Sincronizzazione automatica quando la connessione viene ripristinata
- La cache viene cancellata al logout

### Sicurezza Dispositivo

- Usa la protezione schermata di blocco del dispositivo
- Abilita l'autenticazione biometrica se disponibile
- Mantieni aggiornato il sistema operativo del dispositivo
- Usa reti affidabili per operazioni sensibili

---

## 🚀 Risposta agli Incidenti

### Il Nostro Processo

1. **Rilevamento**: Monitoraggio e segnalazioni utenti
2. **Valutazione**: Valutare gravità e impatto
3. **Contenimento**: Azioni immediate per limitare i danni
4. **Eradicazione**: Rimuovere la vulnerabilità
5. **Recupero**: Ripristinare le operazioni normali
6. **Lezioni Apprese**: Analisi post-incidente

### Notifica Utenti

Notificheremo gli utenti in caso di:
- Violazioni dati che interessano informazioni personali
- Vulnerabilità di sicurezza che richiedono azione immediata
- Aggiornamenti di sicurezza significativi

Metodi di notifica:
- Notifiche in-app
- Email all'indirizzo registrato
- Annuncio pubblico (se appropriato)

---

## 📚 Risorse di Sicurezza

### Per Sviluppatori

- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [Regole di Sicurezza Firebase](https://firebase.google.com/docs/rules)
- [Best Practice Sicurezza React](https://reactjs.org/docs/dom-elements.html#dangerouslysetinnerhtml)

### Per Utenti

- [Guida Sicurezza Password](https://www.agid.gov.it/it/sicurezza/password)
- [Autenticazione a Due Fattori](https://www.agid.gov.it/it/sicurezza/autenticazione-forte)
- [Consapevolezza Phishing](https://www.commissariatodips.it/notizie/articolo/phishing-cose-e-come-difendersi/index.html)

---

## 📞 Contatti

Per problemi o domande sulla sicurezza:

**Contatto Sicurezza**: andreabonacci95@protonmail.com

**Autore**: Andrea Bonacci
- GitHub: [@AndreaBonn](https://github.com/AndreaBonn)

**Tempo di Risposta**: Miriamo a rispondere alle richieste di sicurezza entro 48 ore.

---

## 📝 Changelog Sicurezza

### Versione 1.0.0 (Dicembre 2024)

- ✅ Implementazione Firebase Authentication
- ✅ Deployment Regole di Sicurezza Firestore
- ✅ Applicazione solo HTTPS
- ✅ Controllo accessi basato su ruoli
- ✅ Opzioni crittografia API key
- ✅ Funzionalità sicurezza PWA
- ✅ Validazione e sanitizzazione input
- ✅ Gestione sessioni sicura

---

## 🔄 Aggiornamenti a Questa Politica

Questa politica di sicurezza può essere aggiornata periodicamente. Le modifiche significative saranno annunciate tramite:
- Notifiche in-app
- Aggiornamenti README
- Notifiche email (per modifiche critiche)

**Ultimo Aggiornamento**: Dicembre 2024

---

**[🏠 Torna al README](./README_IT.md)** | **[🇬🇧 English Version](./SECURITY.md)** | **[📄 Licenza](./LICENSE.md)**
