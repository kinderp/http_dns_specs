# 4. Registro delle affermazioni

[Percorso](../README.md) · [Precedente](04-mappa.md) · [Successivo](06-checklist.md)

> **Commento per il docente:** per ogni affermazione confronto un passaggio della fonte, delimito l'ambito e motivo l'esito. La presenza di un link, da sola, non basta.

Controllo documentale svolto con assistenza IA il 2 novembre 2026 sui passaggi indicati. **Verificato** significa sostenuto dal passaggio consultato nell'ambito dichiarato, non approvato dal docente né vero senza condizioni. **Respinto** conserva la traccia di un errore simulato. Le decisioni didattiche non sono fatti dimostrati da una RFC.

| ID e affermazione | Fonte e posizione | Esito della verifica e ambito |
|---|---|---|
| C01 — DNS associa ai nomi informazioni organizzate in record | [R03 §3.6](https://www.rfc-editor.org/rfc/rfc1034.html#section-3.6) | Verificato: il modello comprende tipi di dati differenti, non soltanto indirizzi |
| C02 — In classe Internet, A contiene un indirizzo IPv4; AAAA un indirizzo IPv6 | [R03 §3.6](https://www.rfc-editor.org/rfc/rfc1034.html#section-3.6), [R06 §2.1–2.2](https://www.rfc-editor.org/rfc/rfc3596.html#section-2.1) | Verificato: il tipo distingue il contenuto; non implica corrispondenza uno a uno tra nome e indirizzo |
| C03 — CNAME identifica il nome canonico di un alias | [R03 §3.6](https://www.rfc-editor.org/rfc/rfc1034.html#section-3.6) | Verificato: non è il contenuto HTML |
| C04 — Uno stub resolver può affidare la risoluzione a un servizio ricorsivo | [R03 §5.3.1](https://www.rfc-editor.org/rfc/rfc1034.html#section-5.3.1) | Verificato: è un modello di funzionamento; non descrive ogni implementazione |
| C05 — La cache DNS conserva informazioni per un tempo limitato dal TTL | [R03 §3.6](https://www.rfc-editor.org/rfc/rfc1034.html#section-3.6) | Verificato nel modello introduttivo; non è una cache di pagine web |
| C06 — DNS supporta anche TCP, oltre a UDP | [R04 §1](https://www.rfc-editor.org/rfc/rfc7766.html#section-1) | Verificato: TCP è richiesto per un'implementazione DNS completa; non è una novità da attribuire all'anno del corso |
| C07 — HTTP distingue richieste del client e risposte del server | [M01: sistemi HTTP e messaggi](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Overview#http_messages) | Verificato nel modello client/server considerato |
| C08 — GET richiede una rappresentazione della risorsa individuata | [R01 §9.3.1](https://www.rfc-editor.org/rfc/rfc9110.html#section-9.3.1) | Verificato: non significa “chiedere sempre una pagina HTML” |
| C09 — Una pagina web può richiedere più risorse e quindi più richieste HTTP | [M01: client](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Overview#client_the_user-agent) | Verificato: HTML, stili e immagini sono esempi; “una pagina = una richiesta” è una semplificazione inadeguata |
| C10 — HTTP 404 riguarda una rappresentazione non trovata o non resa nota | [R01 §15.5.5](https://www.rfc-editor.org/rfc/rfc9110.html#section-15.5.5) | Verificato: non è una risposta DNS e non prova un'assenza permanente |
| C11 — HTTP/3 usa QUIC | [R02 §1–2](https://www.rfc-editor.org/rfc/rfc9114.html#section-1) | Verificato: la versione è parte essenziale della frase |
| C12 — HTTP/1.1 è comunemente usato su TCP; HTTP/2 impiega TCP, con TLS per HTTPS | [R02 §1–1.1](https://www.rfc-editor.org/rfc/rfc9114.html#section-1), [R07 §3.2–3.3](https://www.rfc-editor.org/rfc/rfc9113.html#section-3.2) | Verificato con ambito: non trasformare il caso comune HTTP/1.1 in un vincolo universale su ogni possibile trasporto |
| C13 — “DNS usa soltanto UDP” | [R04 §1](https://www.rfc-editor.org/rfc/rfc7766.html#section-1) | Respinto: esclude TCP. Formulazione da usare: C06 |
| C14 — “DNS contiene il file HTML di ogni sito” | R03 §3.6 e M01, collegati sopra | Respinto nel modello del servizio DNS: confonde informazioni sui nomi con rappresentazioni recuperate via HTTP. Formulazione da usare: C01 e C08 |
| C15 — Un Name Error DNS è diverso da HTTP 404 | [R05 §4.1.1, RCODE](https://www.rfc-editor.org/rfc/rfc1035.html#section-4.1.1), R01 §15.5.5 | Verificato: codici di protocolli differenti. Non ogni fallimento DNS è un nome inesistente |
| C16 — “Ogni richiesta HTTP richiede una nuova interrogazione DNS” | R03 §3.6 e M01, collegati sopra | Respinto come regola universale: il riuso di informazioni nella cache basta a fornire un controesempio |
| C17 — Gli studenti della classe conoscono già gli indirizzi IP | Nessuna osservazione della classe reale disponibile | Da verificare: usare D0, non una RFC |
| C18 — È utile un'attività che faccia correggere generalizzazioni | Scelta progettuale motivata da C11–C16 e dal problema ipotizzato | Inferenza didattica: proposta da validare con il docente, non conclusione imposta dalle fonti |

## Ulteriori affermazioni utilizzate nella lezione

| ID e affermazione | Fonte e posizione | Esito della verifica e ambito |
|---|---|---|
| C19 — Un server autorevole fornisce dati per le zone di cui è responsabile | [R03 §4.2](https://www.rfc-editor.org/rfc/rfc1034.html#section-4.2) | Verificato; ruolo distinto dalla ricerca svolta dal resolver |
| C20 — HTTP 200 indica che la richiesta ha avuto successo | [R01 §15.3.1](https://www.rfc-editor.org/rfc/rfc9110.html#section-15.3.1) | Verificato; il contenuto della risposta dipende dal metodo |
| C21 — Il campo Host comunica informazioni sull'host destinatario della richiesta | [R01 §7.2](https://www.rfc-editor.org/rfc/rfc9110.html#section-7.2) | Verificato per l'esempio HTTP/1.1; non estendere il formato a HTTP/2 o HTTP/3 |

## Cosa entra nella specifica

Le voci verificate sostengono i contenuti. Le voci respinte diventano esempi esplicitamente errati, non spiegazioni da insegnare come vere. C17 resta un prerequisito da accertare; C18 motiva una scelta di attività.

Il registro non richiede una riga per ogni ripetizione della stessa frase: deve rendere rintracciabili le affermazioni di contenuto su cui si basa il materiale. Se si aggiungono argomenti, si estende la copertura prima dell'approvazione.
