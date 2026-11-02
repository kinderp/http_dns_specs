# Prove per gli studenti

[Percorso](../README.md) · [Lezione](08-lezione.md)

Scheda distribuibile agli studenti. Casi simulati. Le informazioni necessarie sono nel materiale della lezione; non occorrono strumenti di rete o account personali.

## D0 — Prerequisiti, 5 minuti, senza voto

1. Qual è la differenza intuitiva tra il nome di un host e il suo indirizzo IP?
2. In uno scambio client/server, chi richiede e chi risponde?
3. A che cosa serve, in termini generali, il trasporto nella comunicazione?

Il docente usa le risposte per decidere il recupero, non per presumere che tutti possiedano già queste conoscenze.

## Prova finale — 20 minuti, 20 punti

### P1 — Ruoli (3 punti; 3 minuti)

Attribuisci a DNS o HTTP le due operazioni e spiega la distinzione:
- ottenere informazioni associate al nome corso.example;
- richiedere la rappresentazione della risorsa /lezione.

Correggi la frase: “DNS scarica la pagina HTML”.

### P2 — Record e cache (4 punti; 4 minuti)

Dati simulati, descritti senza rappresentare un file di configurazione:

| Nome | Tipo | Contenuto descritto |
|---|---|---|
| corso.example | A | un indirizzo IPv4 |
| corso.example | AAAA | un indirizzo IPv6 |
| www.corso.example | CNAME | corso.example |

Spiega che cosa significano le tre righe. Se il resolver dispone già di un'informazione valida in cache, deve necessariamente ripetere la stessa interrogazione? Motiva e distingui questa cache dal contenuto della pagina.

### P3 — Richiesta e risposta (4 punti; 4 minuti)

Nel seguente estratto didattico HTTP/1.1 identifica metodo e percorso:
```http
GET /immagine HTTP/1.1
Host: corso.example
```

Il client riceve una risposta HTTP 404. Che cosa puoi concludere? È la stessa cosa di un Name Error ricevuto dal DNS? Spiega perché.

### P4 — Versioni e generalizzazioni (5 punti; 5 minuti)

Completa il confronto HTTP/1.1, HTTP/2, HTTP/3 indicando i trasporti discussi nella lezione e precisando l'ambito di HTTP/1.1. Poi correggi “DNS usa soltanto UDP”, motivando con un riferimento del catalogo o del registro fornito.

### P5 — Caso integrato (4 punti; 4 minuti)

Un browser deve accedere a una risorsa web mediante il nome corso.example. Per il caso base assumiamo cache DNS e web non utilizzabili e nessuna connessione riutilizzabile.

Descrivi il contributo di DNS e HTTP. Spiega cosa cambia con una risposta DNS valida in cache e perché la pagina potrebbe comportare più richieste HTTP. Non sono richiesti dettagli di connessione; indica almeno un limite del modello.

Le fonti possono essere richiamate con ID e sezione. Non è richiesta la memorizzazione dei numeri delle RFC: si valuta la capacità di trovare e usare il riferimento.
