# 1. Catalogo delle fonti

[Percorso](../README.md) · [Precedente](01-scenario.md) · [Successivo](03-selezione.md)

> **Commento per il docente:** assegno un ID a ogni documento e spiego perché lo scelgo. Il catalogo descrive le fonti; gli esiti delle verifiche sono nel registro.

Consultazione dei passaggi utilizzati: **2 novembre 2026**. I numeri di sezione identificano posizioni nel documento, non pagine del manuale. Le RFC storiche sono impiegate per concetti circoscritti e affiancate agli aggiornamenti necessari. Non si dichiara una verifica esaustiva di tutte le errata o di ogni estensione successiva.

| ID | Documento, autori/ente e data | Motivo della scelta e ambito | Posizioni utilizzate |
|---|---|---|---|
| R01 | [RFC 9110 — HTTP Semantics](https://www.rfc-editor.org/rfc/rfc9110.html), Fielding, Nottingham, Reschke, IETF, 2022 | Riferimento normativo per significato di richieste, GET e risposte | §7.2; §9.3.1; §15.3.1; §15.5.5; introduzione |
| R02 | [RFC 9114 — HTTP/3](https://www.rfc-editor.org/rfc/rfc9114.html), Bishop, IETF, 2022 | Distinguere semantica e trasporto; impedire generalizzazioni su TCP | §1, §1.1, §1.2, §2 |
| R03 | [RFC 1034 — Domain Names: Concepts and Facilities](https://www.rfc-editor.org/rfc/rfc1034.html), Mockapetris, 1987 | Concetti DNS, record, cache e resolver; non fotografia di tutte le estensioni odierne | §3.6; §3.6.2; §4.2; §5.3.1; §5.3.3 |
| R04 | [RFC 7766 — DNS Transport over TCP: Implementation Requirements](https://www.rfc-editor.org/rfc/rfc7766.html), Dickinson, Dickinson, Bellis, Mankin, Wessels, IETF, 2016 | Controllare il supporto DNS di TCP | §1; §4 |
| R05 | [RFC 1035 — Domain Names: Implementation and Specification](https://www.rfc-editor.org/rfc/rfc1035.html), Mockapetris, 1987 | Distinguere risposte DNS e codici HTTP | §4.1.1, campo RCODE |
| R06 | [RFC 3596 — DNS Extensions to Support IP Version 6](https://www.rfc-editor.org/rfc/rfc3596.html), Thomson, Huitema, Ksinant, Souissi, IETF, 2003 | Spiegare il record AAAA | §2.1–2.3 |
| R07 | [RFC 9113 — HTTP/2](https://www.rfc-editor.org/rfc/rfc9113.html), Thomson, Benfield, IETF, 2022 | Includere HTTP/2 nel confronto tra versioni | §3.2–3.3 |
| M01 | [MDN — Overview of HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Overview), MDN contributors, pagina in aggiornamento | Esposizione accessibile del modello client/server, delle risorse e dei messaggi | “Components of HTTP-based systems”, “HTTP Messages” |
| H01 | Manuale Hoepli “Sistemi e Reti”, volume 2, Lo Russo e Bianchi, 2013: dati riferiti durante il corso | Possibile supporto alla progressione scolastica | Non consultato; edizione, autori e pagine da controllare sul volume |

## Quattro criteri applicati a tutte le fonti

- **Autorevolezza:** le RFC selezionate sono documenti tecnici primari; MDN è documentazione mantenuta per sviluppatori. Essere sul web non rende automaticamente una fonte meno autorevole.
- **Pertinenza:** le RFC risolvono domande precise; MDN aiuta la spiegazione; un manuale può sostenere prerequisiti e progressione. Nessuna famiglia copre da sola tutti gli usi.
- **Data e ambito:** una data remota non rende falso un concetto. Occorre verificare versioni, aggiornamenti e limiti della frase.
- **Accesso e condizioni d'uso:** colleghiamo le pagine e produciamo spiegazioni originali. Le condizioni sono quelle dei rispettivi siti/documenti. L'accesso non implica il diritto di caricare capitoli o copie integrali.

## Fonti e verifiche

R02 e R04 mantengono gli identificatori della dimostrazione sul trasporto. Gli altri ID valgono all'interno di questo dossier. H01 non sostiene alcuna riga verificata: il percorso completo è riproducibile con fonti pubblicamente consultabili.

Un documento può essere scelto per una verifica ancora da fare. Per sapere se la verifica è stata svolta, leggere il [registro](05-registro.md), non dedurlo dalla presenza nel catalogo.
