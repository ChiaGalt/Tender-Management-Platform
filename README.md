[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/OLXYiqlj)

## React Client Application Routes

- **Route `/`**:
  - **Contenuto della pagina e scopo**: La home page dell'applicazione. Se l'utente non è autenticato, viene reindirizzato alla pagina di login. Se l'utente è autenticato, viene reindirizzato alla pagina della fase corrente (`/phase{phase}`).

- **Route `/login`**:
  - **Contenuto della pagina e scopo**: La pagina di login. Se l'utente è già autenticato, viene reindirizzato alla pagina della fase corrente (`/phase{phase}`).

- **Route `/phase0`**:
  - **Contenuto della pagina e scopo**: Pagina per la fase 0. Accessibile solo se l'utente è autenticato; altrimenti, viene reindirizzato alla pagina di login.

- **Route `/phase1`**:
  - **Contenuto della pagina e scopo**: Pagina per la fase 1. Accessibile solo se l'utente è autenticato; altrimenti, viene reindirizzato alla pagina di login.

- **Route `/phase2`**:
  - **Contenuto della pagina e scopo**: Pagina per la fase 2. Accessibile solo se l'utente è autenticato; altrimenti, viene reindirizzato alla pagina di login.

- **Route `/phase3`**:
  - **Contenuto della pagina e scopo**: Pagina per la fase 3. Accessibile solo se l'utente è autenticato; altrimenti, viene reindirizzato alla pagina di login.

- **Route `*`**:
  - **Contenuto della pagina e scopo**: Rotta  per gestire tutte le rotte non definite. Reindirizza alla home page (`/`).

## API Server

- **POST** `/api/sessions`
  - **Parametri della richiesta e contenuto del body**
    - `username` (string): Username dell'utente.
    - `password` (string): Password dell'utente.
  - **Contenuto del body della risposta**
    - Oggetto utente autenticato.

- **GET** `/api/sessions/current`
  - **Parametri della richiesta e contenuto del body**
    - Nessuno.
  - **Contenuto del body della risposta**
    - Oggetto utente autenticato oppure un errore se non autenticato.
      
- **DELETE** `/api/sessions/current`
  - **Parametri della richiesta e contenuto del body**
    - Nessuno.
  - **Contenuto del body della risposta**
    - Nessuno.

### Budget Sociale APIs

- **POST** `/api/proposals`
  - **Parametri della richiesta e contenuto del body**
    - `text` (string): Testo della proposta.
    - `amount` (integer): Importo della proposta.
  - **Contenuto del body della risposta**
    - Oggetto proposta creata.

- **PUT** `/api/proposals/:id/amount`
  - **Parametri della richiesta e contenuto del body**
    - `id` (integer): ID della proposta.
    - `amount` (integer): Nuovo importo della proposta.
  - **Contenuto del body della risposta**
    - Oggetto proposta aggiornata oppure un errore se non trovata.

- **DELETE** `/api/proposals/:id`
  - **Parametri della richiesta e contenuto del body**
    - `id` (integer): ID della proposta.
  - **Contenuto del body della risposta**
    - Oggetto proposta eliminata oppure un errore se non trovata.

- **GET** `/api/proposals/user/:idUser`
  - **Parametri della richiesta e contenuto del body**
    - `idUser` (integer): ID dell'utente.
  - **Contenuto del body della risposta**
    - Array di oggetti proposta.

- **GET** `/api/proposals/exclude/:idUser`
  - **Parametri della richiesta e contenuto del body**
    - `idUser` (integer): ID dell'utente.
  - **Contenuto del body della risposta**
    - Array di oggetti proposta.

- **GET** `/api/proposals/:id`
  - **Parametri della richiesta e contenuto del body**
    - `id` (integer): ID della proposta.
  - **Contenuto del body della risposta**
    - Oggetto proposta oppure un errore se non trovata.

- **GET** `/api/budget/price`
  - **Parametri della richiesta e contenuto del body**
    - Nessuno.
  - **Contenuto del body della risposta**
    - Oggetto prezzo del budget.

- **PUT** `/api/budget/price`
  - **Parametri della richiesta e contenuto del body**
    - `price` (float): Nuovo prezzo del budget.
  - **Contenuto del body della risposta**
    - Oggetto budget aggiornato oppure un errore se non trovato.
- **GET** `/api/budget/phase`
  - **Parametri della richiesta e contenuto del body**
    - Nessuno.
  - **Contenuto del body della risposta**
    - Oggetto fase del budget.

- **PUT** `/api/budget/phase`
  - **Parametri della richiesta e contenuto del body**
    - `phase` (integer): Nuova fase del budget.
  - **Contenuto del body della risposta**
    - Oggetto budget aggiornato oppure un errore se non trovato.

### Preferences APIs

- **POST** `/api/preferences`
  - **Parametri della richiesta e contenuto del body**
    - `idProposal` (integer): ID della proposta.
    - `score` (integer): Punteggio della preferenza (min: 1, max: 5).
  - **Contenuto del body della risposta**
    - Oggetto preferenza creata.


- **DELETE** `/api/preferences/:id`
  - **Parametri della richiesta e contenuto del body**
    - `id` (integer): ID della preferenza.
  - **Contenuto del body della risposta**
    - Oggetto preferenza eliminata oppure un errore se non trovata.
  

- **GET** `/api/preferences/user/:idUser`
  - **Parametri della richiesta e contenuto del body**
    - `idUser` (integer): ID dell'utente.
  - **Contenuto del body della risposta**
    - Array di oggetti preferenza.

- **GET** `/api/preferences`
  - **Parametri della richiesta e contenuto del body**
    - Nessuno.
  - **Contenuto del body della risposta**
    - Array di oggetti preferenza.

### Proposals APIs

- **GET** `/api/proposals`
  - **Parametri della richiesta e contenuto del body**
    - Nessuno.
  - **Contenuto del body della risposta**
    - Array di oggetti proposta.

### Administrative APIs

- **GET** `/api/users`
  - **Parametri della richiesta e contenuto del body**
    - Nessuno.
  - **Contenuto del body della risposta**
    - Array di oggetti utente.

- **GET** `/api/preferences/grouped`
  - **Parametri della richiesta e contenuto del body**
    - Nessuno.
  - **Contenuto del body della risposta**
    - Array di oggetti preferenza raggruppati per proposta.

- **DELETE** `/api/cleartables`
  - **Parametri della richiesta e contenuto del body**
    - Nessuno.
  - **Contenuto del body della risposta**
    - Messaggio di successo oppure un errore se fallisce.

## Database Tables

- **Tabella `budget`** - contiene `price`, `phase`, `id`
- **Tabella `preferences`** - contiene `id`, `idUser`, `idProposal`, `score`
- **Tabella `proposals`** - contiene `id`, `text`, `amount`, `idUser`
- **Tabella `users`** - contiene `id`, `email`, `hash`, `salt`, `adm`, `name`

## Main React Components

- `LoginForm` (in `Auth.js`): 
  - Scopo: gestisce il processo di login dell'utente.
  - Funzionalità principale: permette agli utenti di autenticarsi inserendo le loro credenziali e naviga alla pagina della fase corrente dopo il login.

- `LogoutButton` (in `Auth.js`): 
  - Scopo: permette agli utenti di effettuare il logout.
  - Funzionalità principale: chiama la funzione di logout passata come prop.

- `LoginButton` (in `Auth.js`): 
  - Scopo: naviga alla pagina di login.
  - Funzionalità principale: reindirizza gli utenti alla pagina di login.

- `Header` (in `Header.js`): 
  - Scopo: mostra l'intestazione dell'applicazione, compreso il logo e i pulsanti di login/logout.
  - Funzionalità principale: mostra l'intestazione con il logo e permette la navigazione tra le sezioni dell'applicazione in base allo stato di autenticazione dell'utente.

- `Home` (in `Home.js`): 
  - Scopo: pagina principale dell'applicazione.
  - Funzionalità principale: mostra una panoramica delle fasi del budget e permette la navigazione verso le sezioni pertinenti.

- `Phase0` (in `Phase0.js`): 
  - Scopo: gestisce e visualizza i contenuti della fase 0.
  - Funzionalità principale: permette di visualizzare e aggiornare il budget, e consente agli amministratori di passare alla fase 1.

- `Phase1` (in `Phase1.js`): 
  - Scopo: gestisce e visualizza i contenuti della fase 1.
  - Funzionalità principale: permette agli utenti di aggiungere, modificare ed eliminare proposte, e consente agli amministratori di passare alla fase 2.

- `Phase2` (in `Phase2.js`): 
  - Scopo: gestisce e visualizza i contenuti della fase 2.
  - Funzionalità principale: Mostra le proposte provenienti dagli altri utenti.
  Gestisce l'aggiunta e la rimozione delle preferenze degli utenti sulle proposte.
  Permette agli amministratori di avanzare alla fase 3.

- `Phase3` (in `Phase3.js`): 
  - Scopo: gestisce e visualizza i contenuti della fase 3.
  - Funzionalità principale: Mostra le proposte approvate e non approvate agli utenti, quelle solo approvati agli anonimi.
  Consente agli amministratori di resettare il sistema tornando alla fase 0.

## Screenshot

![Fase 1 - user](image.png)
![Fase 2 - admin](image-1.png)
## Users Credentials

- mario.rossi@noprofit.it, password: marioRossi ADMIN
- john.smith@noprofit.it, password: johnSmith
- tony.stark@noprofit.it, password: tonyStark
- john.lee@noprofit.it, password: johnLee
