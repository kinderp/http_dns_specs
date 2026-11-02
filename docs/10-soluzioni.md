# Soluzioni motivate e rubrica

[Percorso](../README.md) · [Prove](09-prove-studenti.md) · [Registro](05-registro.md)

Materiale per il docente, da separare dalla scheda studenti durante la prova. Accettare formulazioni equivalenti e motivate; non richiedere riproduzioni letterali.

## D0 — Lettura diagnostica

Nome e indirizzo non sono sinonimi; client e server sono ruoli di richiesta/risposta; il trasporto sostiene la comunicazione tra estremi. Una spiegazione intuitiva corretta è sufficiente. La classe è fittizia: queste risposte attese non sono osservazioni già raccolte.

## S1 — Soluzione P1, 3 punti

DNS: informazioni sul nome. HTTP: richiesta della rappresentazione della risorsa. L'HTML non viene scaricato dal servizio DNS nel modello della lezione. Fonti: C01, C07, C08.

Punteggio: 1 punto per ciascuna attribuzione corretta; 1 per la correzione motivata.

## S2 — Soluzione P2, 4 punti

A indica un indirizzo IPv4; AAAA un IPv6; CNAME indica un alias verso un nome canonico. Con informazioni DNS valide in cache non è necessariamente richiesta una nuova interrogazione. La cache DNS non contiene per questo la pagina web. Fonti: C02, C03, C05.

Punteggio: 1 per ciascun tipo correttamente interpretato; 1 per riuso motivato della cache e distinzione dalla pagina. Per l'ultimo punto assegnare 0,5 se è presente solo una delle due componenti.

## S3 — Soluzione P3, 4 punti

Metodo GET; percorso /immagine. 404 indica che la rappresentazione non è stata trovata o non viene resa nota; non certifica che l'assenza sia permanente. Il Name Error DNS riguarda invece il nome e appartiene a un altro protocollo. Un silenzio o un timeout da solo non equivale a Name Error. Fonti: C08, C10, C15.

Punteggio: 1 metodo; 1 percorso; 1 significato essenziale di 404; 1 distinzione motivata dal DNS. Non è indispensabile ricordare la possibilità di non divulgazione per ottenere il punto su 404, purché non si affermi un'assenza definitiva o un errore DNS.

## S4 — Soluzione P4, 5 punti

HTTP/1.1 è comunemente usato su TCP; HTTP/2 usa TCP (TLS per HTTPS); HTTP/3 usa QUIC. DNS può usare anche TCP oltre a UDP. R04 §1 sostiene la correzione di “soltanto UDP”; C06 ne registra la verifica. Fonti del confronto: C11, C12.

Punteggio: 1 per ciascuna versione e relativo ambito (3); 1 per correggere DNS; 1 per motivazione e riferimento pertinente. Per HTTP/1.1 assegnare 0,5 se il trasporto è riconosciuto ma formulato come obbligo universale.

## S5 — Soluzione P5, 4 punti

Nel caso dato si ottengono informazioni sul nome, poi si effettua lo scambio HTTP della risorsa. Una cache DNS valida può evitare di ripetere la ricerca; non elimina per ciò stesso lo scambio HTTP. Una pagina può richiedere altre risorse. Il modello omette dettagli e non vale come sequenza identica in tutte le situazioni. Fonti: C05, C07–C09, C16.

Punteggio: 1 distinzione funzionale; 1 variante cache; 1 risorse multiple; 1 limite esplicito del modello.

## Interpretazione dei risultati

Totale: **3 + 4 + 4 + 5 + 4 = 20 punti**. Soglia proposta: 14/20, da approvare e adattare alla classe. Non basta il totale: segnalare comunque gli obiettivi critici non dimostrati.

| Obiettivo | Riscontro da leggere | Indicazione per il recupero |
|---|---|---|
| O01 | P1; distinzione dei ruoli in P5 | Riprendere nome e rappresentazione |
| O02 | P2 | Separare tipo di record, indirizzo e cache |
| O03 | P3 | Annotare un nuovo messaggio e confrontare gli errori |
| O04 | P4, prime tre componenti | Ricostruire la tabella versioni/trasporti |
| O05 | P5 | Rifare il caso dichiarando le ipotesi |
| O06 | Motivazione in P4 e limiti in P5 | Collegare correzione e passaggio della fonte |

Una buona risposta alla prova non certifica competenze di configurazione o diagnosi reale di rete, che sono fuori ambito.
