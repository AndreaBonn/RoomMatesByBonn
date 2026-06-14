# Politica di Sicurezza

[English](./SECURITY.md) | **Italiano**

## Versioni supportate

| Versione | Supportata |
|---|---|
| 1.0.x | ✅ Aggiornamenti di sicurezza |
| < 1.0 | ❌ Fine vita |

Le correzioni di sicurezza vengono applicate alla release corrente. Gli utenti vengono avvisati degli aggiornamenti critici tramite l'applicazione.

## Segnalare una vulnerabilità

Non aprire una issue pubblica su GitHub per problemi di sicurezza.

Segnala in privato tramite i [GitHub Security Advisories](https://github.com/AndreaBonn/RoomMatesByBonn/security/advisories/new), oppure via email all'indirizzo andreabonacci95@protonmail.com con oggetto `SECURITY: <breve descrizione>`.

Includi:

- Una descrizione della vulnerabilità
- I passi per riprodurla
- Il comportamento atteso rispetto a quello osservato
- Una valutazione dell'impatto (cosa potrebbe ottenere un attaccante)

Tempi di risposta:

- Conferma di ricezione entro 72 ore
- Valutazione della gravità entro 5 giorni lavorativi
- Divulgazione pubblica coordinata dopo il rilascio della correzione

Non è previsto un programma di bug bounty formale.

## Misure di sicurezza implementate

Queste sono le protezioni presenti nell'applicazione. I riferimenti ai file rimandano al sorgente dell'applicazione, che è privato.

- **Controllo degli accessi al database**: le Firestore Security Rules circoscrivono ogni lettura e scrittura alla casa di cui l'utente fa parte, con controlli di ruolo per proprietario, admin e membro (`firestore.rules`)
- **Autenticazione**: Firebase Authentication con email e password; i token di sessione sono gestiti dall'SDK Firebase
- **Header HTTP di sicurezza**: Content-Security-Policy stretta (`default-src 'self'`, `object-src 'none'`, allowlist esplicite per connect e frame), HSTS con `preload` e max-age di un anno, `X-Frame-Options: DENY`, `X-Content-Type-Options: nosniff`, `Referrer-Policy` e una `Permissions-Policy` che disabilita camera, microfono e geolocalizzazione (`firebase.json`)
- **Sicurezza del trasporto**: solo HTTPS, servito da Firebase Hosting, con `upgrade-insecure-requests` nella CSP
- **Hardening del servizio email**: Helmet per gli header di risposta, una allowlist CORS e rate limiting sull'invio con un limite giornaliero globale e uno per casa (`email-service/server.js`, `email-service/middleware/rate-limit.js`)
- **Chiavi API per l'AI**: salvate nel browser o su Firestore a scelta dell'utente; la direttiva `connect-src` della CSP limita gli endpoint dei provider che il client può chiamare
- **Monitoraggio degli errori**: Sentry raccoglie gli errori a runtime per la diagnosi

L'applicazione usa un database NoSQL (Firestore), quindi la SQL injection non si applica. L'output è renderizzato tramite React, che effettua l'escape dei contenuti per impostazione predefinita.

## Best practice per gli utenti

- Usa una password robusta e unica e mantieni sicuro il tuo account email, perché viene usato per il recupero della password
- Condividi i codici di invito della casa solo con persone fidate e rigenerali se vengono esposti
- Mantieni private le chiavi API dei provider AI; preferisci il salvataggio nel browser e imposta limiti di utilizzo sul tuo account provider
- Rimuovi i membri che non vivono più nella casa
- Esci dall'account sui dispositivi condivisi

## Fuori ambito

I seguenti casi non sono trattati come vulnerabilità:

- Self-XSS che richiede alla vittima di incollare codice nella propria console
- Attacchi di social engineering
- Attacchi fisici a dispositivi o infrastruttura
- Vulnerabilità in servizi di terze parti (Firebase, Brevo, provider AI); vanno segnalate al rispettivo fornitore
- Denial of service tramite uso legittimo eccessivo

## Riconoscimenti

I ricercatori di sicurezza che divulgano responsabilmente le vulnerabilità verranno elencati qui.

---

[Torna al README](./README_IT.md)
