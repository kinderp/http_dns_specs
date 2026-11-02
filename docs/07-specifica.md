# 6. Specifica completa della lezione DNS e HTTP

[Percorso](../README.md) · [Precedente](06-checklist.md) · [Applicazione: lezione](08-lezione.md)

> **Commento per il docente:** passo da “che cosa sappiamo” a “che cosa deve contenere il prodotto”. Il docente definisce requisiti e criteri, usando conoscenze verificate, destinatari, obiettivi e vincoli.

**SPEC-DNS-HTTP 1.0 — proposta da approvare.**
Prodotto richiesto: materiale per una lezione introduttiva completa, con guida di conduzione, attività, prova finale, soluzioni motivate e riferimenti. Destinatari e assunzioni sono nello [scenario](01-scenario.md). Non è la sola mini-specifica di 20 minuti sul trasporto.

## Intento

Permettere agli studenti di spiegare i ruoli complementari di DNS e HTTP in un accesso web semplificato, interpretare informazioni essenziali e riconoscere generalizzazioni scorrette.

## Obiettivi e prestazioni osservabili

| ID | Al termine lo studente saprà… | Evidenza di apprendimento prevista |
|---|---|---|
| O01 | Distinguere il ruolo di DNS da quello di HTTP | P1: attribuire operazioni al protocollo e motivare |
| O02 | Interpretare A, AAAA e CNAME e spiegare l'effetto di una cache valida | P2: leggere dati simulati e descrivere il riuso |
| O03 | Riconoscere metodo, risorsa e risposta in uno scambio HTTP | P3: annotare una richiesta GET e distinguere 404 da un errore DNS |
| O04 | Distinguere versioni HTTP e trasporti senza assoluti impropri | P4: completare il confronto e correggere “solo UDP” |
| O05 | Descrivere un caso web dichiarando le semplificazioni | P5: collegare risoluzione, richiesta, risposta e risorse aggiuntive |
| O06 | Correggere un'affermazione errata con motivazione e riferimento | P4 e P5: spiegazione sostenuta dal registro |

La prestazione è ciò che osserviamo; la prova è il compito che la rende osservabile. La presenza della prova nel materiale non dimostra che gli studenti abbiano già raggiunto l'obiettivo.

## Prerequisiti e vincoli

- Classe quarta fittizia; D0 accerta IP, client/server e trasporto.
- Durata proposta: 90 minuti, 45 + 45. Se il recupero non basta, ripianificare prima dell'uso.
- Linguaggio introduttivo con glossario; colori mai unico veicolo del significato.
- Schede leggibili offline; niente accessi a account personali o traffico reale.
- Solo dati fittizi; nessun nominativo, risultato individuale o log di studenti nel repository.
- Fonti collegate e sintesi originali; nessun capitolo del manuale copiato.
- La lezione non deve presentare come certe ipotesi sulla classe o decisioni ancora aperte.
- Fuori ambito: UDA completa, configurazione server, analisi di pacchetti e dettagli delle estensioni DNS.

## Requisiti del materiale

| ID | Requisito obbligatorio | Origine |
|---|---|---|
| REQ01 | Spiegare DNS e HTTP con un confronto e un caso in cui si vedono entrambi | O01; C01, C07–C09 |
| REQ02 | Distinguere nome, record, resolver e server autorevole; includere A/AAAA/CNAME e cache | O02; C01–C05 |
| REQ03 | Includere una richiesta GET didattica, una risposta e l'interpretazione di 404 | O03; C07, C08, C10 |
| REQ04 | Separare errore DNS e risposta HTTP senza diagnosticare ogni guasto come NXDOMAIN | O03; C15 |
| REQ05 | Confrontare HTTP/1.1, HTTP/2, HTTP/3 e DNS rispetto al trasporto, indicando l'ambito | O04; C06, C11, C12 |
| REQ06 | Includere correzioni motivate di almeno due generalizzazioni simulate | O06; C13–C16 |
| REQ07 | Esplicitare ipotesi e limiti del caso web, comprese cache e risorse multiple | O05; C05, C09, C16 |
| REQ08 | Prevedere diagnosi dei prerequisiti e recupero o ripianificazione | C17; scelta docente |
| REQ09 | Fornire prove coerenti con tutti gli obiettivi e soluzioni con rubrica | O01–O06 |
| REQ10 | Rispettare durata, accessibilità, dati fittizi e uso delle fonti | Vincoli di progetto |

## Criteri di accettazione e metodi di prova

Un criterio di accettazione è una condizione verificabile per decidere se il materiale soddisfa la specifica. La colonna evidenza indica dove guardare, non un esito già garantito.

| ID | Condizione di accettazione | Metodo di controllo ed evidenza attesa |
|---|---|---|
| AC01 | Il materiale distingue ricerca di informazioni sul nome e recupero della risorsa | Leggere L1 e P1, confrontare soluzione S1 con C01/C08; respingere attribuzione dell'HTML al DNS |
| AC02 | Record, resolver e cache sono spiegati con almeno un esempio coerente | Controllare L2, P2/S2 e C01–C05; verificare che cache DNS e cache web non siano confuse |
| AC03 | L'esempio HTTP permette di identificare metodo, risorsa e codice di risposta | Eseguire P3 usando L3, verificare S3 contro C07/C08/C10 |
| AC04 | Il materiale distingue Name Error DNS da 404 e non rende equivalenti tutti i guasti | Leggere L3 e S3; controllare C15 |
| AC05 | Il confronto include tutte e tre le versioni HTTP e DNS su UDP/TCP | Leggere L4 e P4/S4; confrontare C06/C11/C12; cercare eventuali “sempre TCP” o “solo UDP” presentati come fatti |
| AC06 | Almeno due idee sbagliate hanno correzione, motivazione e fonte | Contare in S4/S5; risalire a C13–C16 e alle fonti |
| AC07 | Il caso dichiara condizioni iniziali e almeno due limiti | Leggere L5, P5/S5; verificare esplicitazione di cache e risorse aggiuntive |
| AC08 | Diagnosi e recupero dei prerequisiti sono attuabili | Eseguire D0 sulla carta; controllare regola di recupero nel piano |
| AC09 | Ogni obiettivo ha una prova, soluzione e criterio di punteggio | Seguire O01–O06 verso P1–P5 e rubrica; sommare i punteggi |
| AC10 | Il piano totalizza 90 minuti e le schede sono utilizzabili senza dati personali o rete | Sommare intervalli del piano; leggere materiali offline; controllare assenza di dati reali |

Per ogni AC si registra **soddisfatto / non soddisfatto / non valutabile**, evidenza e intervento. Un criterio non valutabile non è automaticamente soddisfatto. Il docente approva la versione dopo il controllo.

## Tracciabilità essenziale

| Conoscenze / scelta | Obiettivo | Requisiti | Accettazione | Materiale / prova |
|---|---|---|---|---|
| C01, C07, C08 | O01 | REQ01 | AC01 | L1; P1/S1 |
| C01–C05 | O02 | REQ02 | AC02 | L2; P2/S2 |
| C07, C08, C10, C15 | O03 | REQ03–04 | AC03–04 | L3; P3/S3 |
| C06, C11, C12 | O04 | REQ05 | AC05 | L4; P4/S4 |
| C05, C09, C16 | O05 | REQ07 | AC07 | L5; P5/S5 |
| C13–C16 | O06 | REQ06 | AC06 | L4–L5; P4/P5 e soluzioni |
| C17 e vincoli | Trasversale | REQ08–10 | AC08–10 | D0, piano, rubrica |

## Approvazione e cambiamenti

Versione proposta con IA; approvazione docente aperta. Una modifica alle fonti può richiedere aggiornamenti al registro, alla mappa, ai requisiti e alle prove. Una modifica alla durata può richiedere una riduzione esplicita degli obiettivi: non basta tagliare minuti lasciando invariati i criteri.

[Decisioni e questioni aperte](12-decisioni.md) · [Revisione](11-revisione.md)
