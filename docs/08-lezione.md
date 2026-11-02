# 7. Lezione completa: DNS e HTTP nell'accesso a una risorsa web

[Percorso](../README.md) · [Specifica](07-specifica.md) · [Prove studenti](09-prove-studenti.md) · [Soluzioni](10-soluzioni.md)

> **Commento per il docente:** questo è un esempio di prodotto realizzato dalla specifica. Ora possiamo controllare il materiale con gli AC. L'apprendimento sarà verificabile solo quando gli studenti risponderanno alle prove.

Bozza didattica per 90 minuti. Ogni sezione richiama il [registro](05-registro.md), che contiene le fonti e i limiti delle affermazioni. Le osservazioni sulla classe sono ancora da raccogliere.

## Piano di conduzione

| Minuti | Attività e conduzione | Risultato osservabile |
|---|---|---|
| 0–5 | D0: tre domande individuali sui prerequisiti | Risposte iniziali, non valutazione sommativa |
| 5–10 | Recupero su IP, client/server e trasporto; se non necessario, applicazione a un esempio | Lessico minimo condiviso |
| 10–20 | L1: confronto dei ruoli; due attribuzioni orali motivate | Distinzione DNS/HTTP |
| 20–35 | L2: record, resolver, cache; lettura guidata della tabella | Interpretazione delle informazioni |
| 35–45 | L3: richiesta e risposta, confronto degli errori | Riconoscimento delle parti del messaggio |
| 45–55 | L4: versioni e trasporti; correzione collettiva di un assoluto | Versione e ambito espliciti |
| 55–65 | L5: caso integrato a coppie, con variante cache | Relazioni motivate e limiti del modello |
| 65–85 | P1–P5 individuali | Risposte per O01–O06 |
| 85–90 | Restituzione essenziale e indicazione del recupero | Errori da rivedere e passi successivi |

Totale: **90 minuti**. Le due unità da 45 possono svolgersi in incontri distinti. La correzione dettagliata delle prove è lavoro successivo del docente; negli ultimi cinque minuti si discutono le risposte chiave, non ogni elaborato.

D0: se almeno una risposta mostra confusione sui termini essenziali, usare il blocco di recupero. Se dopo il recupero la classe non riesce ancora a distinguere nome e indirizzo o client e server, interrompere la progressione tecnica e ripianificare: i 90 minuti non sono una promessa indipendente dai prerequisiti.

## L1 — Due domande, due ruoli

Domanda iniziale: “Conoscere il nome di un sito significa già avere il contenuto della pagina?”

DNS permette di ottenere informazioni associate a un nome. HTTP organizza richieste e risposte per accedere a risorse. Sono ruoli complementari. Un nome non è un file e una risposta DNS non è la pagina HTML.

| Domanda | Ruolo in questo esempio |
|---|---|
| Quali informazioni di indirizzamento sono associate al nome? | DNS |
| Quale rappresentazione della risorsa viene richiesta? | HTTP |
| Chi presenta la pagina all'utente? | Il browser interpreta e combina le risorse ricevute |

Far attribuire agli studenti due operazioni: “cercare un record relativo al nome” e “richiedere una risorsa con GET”. Chiedere una motivazione, non solo una sigla. Riferimenti: C01, C07, C08.

## L2 — Record, resolver e cache

Il DNS non è soltanto un elenco di coppie nome/indirizzo. I record hanno tipi diversi. In questa lezione:

| Tipo | Informazione | Lettura didattica |
|---|---|---|
| A | Indirizzo IPv4 | Un indirizzo associato al nome |
| AAAA | Indirizzo IPv6 | Un indirizzo IPv6 associato al nome |
| CNAME | Nome canonico di un alias | Il nome rinvia a un altro nome, non a un file HTML |

Il resolver cerca la risposta per il richiedente. Nello scenario, il componente locale si appoggia a un servizio ricorsivo. Un server autorevole fornisce i dati delle zone di cui è responsabile. Non sono sinonimi; un sistema può svolgere più ruoli, ma la distinzione funzionale resta utile.

La cache DNS conserva informazioni già ottenute per un intervallo regolato dal TTL. Non è il contenuto della pagina web. Perciò una nuova richiesta HTTP non richiede necessariamente una nuova interrogazione DNS.

Esempio da discutere: abbiamo un'informazione di indirizzamento ancora valida in cache. Possiamo riutilizzarla; ciò non significa che abbiamo già scaricato l'immagine richiesta. Riferimenti: C01–C05, C19.

## L3 — Richiesta, risposta ed errore

Rappresentazione **didattica parziale** di un messaggio HTTP/1.1; non è una cattura di rete e non va usata come descrizione del formato sul filo di HTTP/2 o HTTP/3.

```http
GET /lezione HTTP/1.1
Host: corso.example
```

Il metodo è GET; la destinazione della richiesta nell'esempio è il percorso /lezione; il campo Host specifica il nome dell'host. Non stiamo inviando l'intero URL come domanda al DNS.

Un estratto della risposta, sempre parziale e didattico, può essere:

```http
HTTP/1.1 404 Not Found
Content-Type: text/html
```

Sono omessi il corpo e i dettagli di delimitazione del messaggio. Una risposta può avere stato 200, indicando successo, oppure 404. Quest'ultimo riguarda la rappresentazione della risorsa non trovata o non resa nota: non significa automaticamente “il nome DNS non esiste”.

Confronto per ragionare:

- Il resolver restituisce Name Error: il problema segnalato riguarda il nome richiesto.
- Si riceve una risposta HTTP 404: è arrivata una risposta HTTP relativa alla risorsa.
- Non arriva alcuna risposta: non basta questo dato per scegliere una sola causa.

Riferimenti: C07, C08, C10, C15, C20, C21. Non insegnare che tutti gli errori DNS equivalgono a Name Error.

## L4 — Stesso ambito applicativo, versioni e trasporti diversi

| Caso | Trasporto da distinguere | Precisazione |
|---|---|---|
| HTTP/1.1 | Comunemente TCP | Non estendere il caso comune a ogni versione e possibilità |
| HTTP/2 | TCP; TLS quando usato con HTTPS | Non confondere versione e protezione |
| HTTP/3 | QUIC | La frase deve specificare HTTP/3 |
| DNS | UDP e anche TCP | “Soltanto UDP” è scorretto |

Esercizio orale: correggere “HTTP usa sempre TCP”. Una correzione adeguata precisa le versioni. Correggere poi “DNS usa soltanto UDP”, citando la fonte che documenta TCP. Riferimenti: C06, C11–C13.

Non occorre spiegare qui i dettagli di QUIC, handshake, cifratura o multiplexing. L'obiettivo è distinguere ruoli e ambiti senza assoluti ingiustificati.

## L5 — Il caso integrato e i suoi limiti

Caso simulato: il browser deve accedere a una risorsa identificata da un nome. Assumiamo assenza di informazioni DNS utilizzabili in cache, nessuna connessione riutilizzabile e nessuna risposta già disponibile nella cache web. Omettiamo proxy, negoziazione e dettagli della connessione.

1. Il componente di risoluzione ottiene le informazioni necessarie sul nome.
2. Il client stabilisce la comunicazione adatta alla versione HTTP considerata.
3. Invia la richiesta della risorsa.
4. Riceve una risposta e ne interpreta lo stato.
5. La rappresentazione ricevuta può richiedere risorse aggiuntive, ad esempio immagini.

Questa è una **sintesi didattica condizionata**, non una sequenza universale. Chiedere alle coppie che cosa cambia se la cache DNS contiene informazioni valide. Poi chiedere perché “una pagina = una sola richiesta” può fallire.

Non è richiesto uno schema grafico specifico: sono accettabili testo, frecce commentate o una tabella, purché relazioni e limiti siano espliciti. Riferimenti: C05, C07–C09, C16.

## Chiusura e riuso

Somministrare le [prove](09-prove-studenti.md) senza allegare le soluzioni. Usare la [rubrica](10-soluzioni.md) per distinguere gli obiettivi raggiunti da quelli da riprendere. Aggiornare [le decisioni](12-decisioni.md) con evidenze aggregate e prive di dati identificativi, se si decide di documentare la sperimentazione.
