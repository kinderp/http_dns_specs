# DNS e HTTP: dalle fonti alla specifica della lezione

Un esempio completo per docenti: come costruire una base di conoscenze, ricavarne una specifica e controllare il materiale didattico prodotto.

**Ambito:** intera lezione introduttiva su DNS e HTTP, non soltanto il trasporto. Ruoli, nomi e record, risoluzione e cache, richiesta e risposta, risorse web, versioni e trasporti, errori tipici.

**Versione 1.0 — 2 novembre 2026.** Dossier predisposto con assistenza IA e consultazione dei passaggi tecnici citati. Approvazione didattica del docente e sperimentazione in classe ancora da effettuare. Nessun risultato di apprendimento è dichiarato già raggiunto.

## Parti del percorso

| Passo | Attività: che cosa facciamo e perché | Artefatto prodotto |
|---|---|---|
| 0 | Definiamo il problema e distinguiamo dati disponibili e ipotesi | [Scenario e decisioni iniziali](docs/01-scenario.md) |
| 1 | Scegliamo fonti pertinenti, identificabili e consultabili; motiviamo ogni scelta | [Catalogo delle fonti](docs/02-catalogo.md) |
| 2 | Leggiamo i passaggi utili e selezioniamo informazioni per la lezione | [Appunti di selezione](docs/03-selezione.md) |
| 3 | Rendiamo espliciti concetti e relazioni | [Mappa](docs/04-mappa.md) |
| 4 | Confrontiamo le affermazioni con le fonti e registriamo esiti e limiti | [Registro delle affermazioni](docs/05-registro.md) |
| 5 | Controlliamo completezza, evidenze e questioni aperte | [Checklist della base di conoscenze](docs/06-checklist.md) |
| 6 | Il docente traduce conoscenze, obiettivi e vincoli in requisiti e prove | [Specifica completa](docs/07-specifica.md) |
| 7 | Produciamo un esempio di materiale coerente con la specifica | [Lezione e conduzione](docs/08-lezione.md), [prove studenti](docs/09-prove-studenti.md), [soluzioni](docs/10-soluzioni.md) |
| 8 | Registriamo la revisione del registro, della specifica e del materiale, separatamente | [Scheda di revisione](docs/11-revisione.md) |
| 9 | Conserviamo decisioni, limiti e modifiche per il riuso | [Questioni aperte e aggiornamenti](docs/12-decisioni.md) |

La **base di conoscenze** è formata da catalogo, mappa e registro. Gli appunti documentano il lavoro di selezione; la checklist è lo strumento per riesaminare la raccolta. Non ogni attività richiede un documento autonomo: qui separiamo i file per rendere visibile il processo formativo.

La **specifica** descrive ciò che dovrà essere realizzato e come accettarlo. La **lezione** è il materiale che la realizza. Le **prove degli studenti** valutano l'apprendimento; i **criteri di accettazione** valutano il materiale. Non sono lo stesso controllo.

## Come usare questo repository

1. Leggere scenario, catalogo e registro; aprire almeno i passaggi che sostengono le affermazioni decisive.
2. Consultare la specifica e seguire un collegamento completo: C11 → REQ05 → AC05 → lezione L4 → prova P4.
3. Mostrare la scheda di revisione: una fonte rintracciabile non equivale automaticamente a una decisione approvata.
4. Adattare durata, destinatari, accessibilità e soglie alla classe reale, registrando le modifiche.
5. Usare le prove senza distribuire contestualmente le soluzioni.

La proposta completa dura **90 minuti, in due unità da 45**, come scelta progettuale da approvare. I **20 minuti** concordati nella dimostrazione dal vivo riguardano invece la mini-specifica sul trasporto: non sono la durata della lezione completa.

Per la dimostrazione guidata usare [il percorso breve](docs/13-dimostrazione-dal-vivo.md). Per un nuovo argomento usare [il modello compilabile](modelli/percorso.md).

## Tracciabilità e lettura

- R e M identificano fonti; C identifica affermazioni; O obiettivi; REQ requisiti; AC criteri di accettazione; P prove; Q questioni aperte.
- Una riga del registro può avere più fonti. La “scheda evidenza” non è un artefatto distinto: qui si parla sempre di voce del registro.
- Le mappe Mermaid si visualizzano su GitHub; la tabella sottostante offre la stessa informazione testuale.
- Tutti i materiali sono in Markdown UTF-8 e si leggono anche senza programmi dedicati.
- [Glossario](docs/14-glossario.md) e [resoconto dei controlli](CONTROLLI.md).

## Provenienza e uso dei contenuti

Le spiegazioni e gli esercizi sono redatti per questo esempio; i casi sono simulati. Non sono estratti da un manuale. Le fonti esterne sono collegate, non ripubblicate integralmente. Il manuale menzionato durante il corso resta un riferimento facoltativo non consultato qui: nessuna frase o pagina gli viene attribuita.

Il repository non assegna automaticamente una licenza alle fonti esterne. La licenza dei materiali originali del corso è una decisione del titolare ancora aperta: consultare [le decisioni](docs/12-decisioni.md) prima di riusi ulteriori. Non sono presenti dati reali di studenti.
