# Time Machine Project | Replica cinematografica 1:1

Progetto di ricostruzione artigianale a grandezza naturale della **macchina del tempo del film di George Pal (1960)**. L'obiettivo è realizzarla fisicamente con falegnami, carpentieri, tornitori, tappezzieri e altri artigiani. **Non è un progetto di stampa 3D.**

## Stato del progetto

**Fase: documentazione e pre-progettazione (REV14, 11 novembre 2026).** Nessun disegno è ancora approvato per la fabbricazione.

| Sottoassieme | Stato | Prossima attività |
| --- | --- | --- |
| Basamento in legno | REV04: dossier 10 tavole, 4 schede dime, protocollo campioni; NON esecutivo | Rilievo quote, dime reali, giunzioni e verifica struttura |
| Quattro piedi ornamentali | REV14: 4 STL volumetrici artistici autonomi (SX/DX, 2 profondità), 8 tavole A3, audit Bézier risolto; **non sono piedi completi né CNC** | Confermare superfici MGM, corrispondenza viste, acciaio/ruote, gusci e giunti da progettare |
| Sedia Berninghaus | REV05: dossier 8 tavole, quote grafiche di riscontro, schede falegname e tappezziere; NON esecutivo | Rilievo quote reali, mock-up, giunti e portata |
| Grande disco posteriore | Rilevata discrepanza dimensionale tra riferimento Coleman e OBJ | Validare diametro e riprogettare geometria |
| Corrimano e struttura | Riferimenti di metodo costruttivo | Sezioni, dime di curvatura e attacchi |
| Console e comandi | Riferimenti di processo | Elaborati per tornitura, incisioni e componenti |

### Ultima revisione

- **[REV14: 4 ricci artistici in 3D e rettifica quote Bézier](docs/REV14_RICCI_ARTISTICI_3D.md)** · [REV13: pannelli 2.5D](docs/REV13_RILIEVI_2_5D.md) · [REV12: curve vettoriali Perrotta](docs/REV12_VETTORI_PERROTTA_CNC.md) · [REV11A: precedenti stime grafiche](docs/REV11A_QUOTE_PERROTTA.md) · [REV11: schede officina e controlli](docs/REV11_RILIEVO_OFFICINA_CNC.md) · [REV10: generatore parametrico](docs/REV10_RILIEVO_SUPPORTI_PARAMETRICO.md) · [REV09 solidi di prova](docs/REV09_SOLIDI_PROTOTIPO_CNC.md) · [REV08: superfici dei piedi](docs/REV08_PIEDI_LEGNO_CNC.md) · [REV07 carpenteria](docs/REV07_TELAIO_PIEDI.md) · [REV06 interfaccia sedia/basamento](docs/REV06_INTERFACCIA_SEDIA_BASE.md) · [REV05 sedia Berninghaus](docs/REV05_SEDIA_BERNINGHAUS.md), con PDF/ZIP su Drive privato. Nessun OBJ su GitHub.

### Indice dei materiali e delle fonti
- **[Tutte le risorse create, PDF, DXF e ZIP su Drive](docs/ARCHIVIO_RISORSE.md)**, con revisione, contenuti degli archivi e indicazione dei file contenenti OBJ.
- **[Fonti originali e metodo Don Coleman](docs/FONTI.md)**, incluse le pagine relative a basamento, sedia, console, piedi, carter e corrimano, e la tavola Perrotta/Coleman.
- **[Catalogo risorse CSV con link](data/catalogo_risorse.csv)**, per cercare e filtrare i materiali.

[REV04 basamento](docs/REV04_BASAMENTO_FALEGNAMERIA.md) · [Registro di avanzamento](docs/AVANZAMENTO.md) · [Registro quote](data/registro_quote.csv) · [Revisioni](docs/REVISIONI.md) · [Metodo Coleman](docs/METODO_COLEMAN.md)

## Regole del progetto

1. **Fedeltà cinematografica:** riferimento principale ai disegni di Chris Perrotta rivisti da Don Coleman e alle fonti del prop MGM.
2. **Metodo costruttivo Coleman:** riprendere dove documentato materiali, lavorazioni e sequenze, senza trasformare esempi di replica in quote automaticamente vincolanti per il prop originale.
3. **Doppia quotatura:** nei disegni destinati agli artigiani italiani le quote operative sono in **mm**; i valori originali in **pollici** sono riportati accanto. 1″ = 25,4 mm.
4. **Provenienza delle quote:** **D** = documentata; **G** = derivata dalla geometria OBJ; **I** = ipotesi di progetto; **V** = da verificare. Non mescolare categorie senza avvertenza.
5. **Sicurezza:** struttura portante, piedini, sedia occupabile e disco richiedono verifica e progettazione da parte di professionisti qualificati prima della produzione.

## Questioni dimensionali aperte

- L'OBJ precedentemente calibrato restituisce ingombri di circa **2475 × 1953 × 2635 mm** (L × P/larghezza × H). Questi dati **non sono dimensioni originali certificate**.
- Il basamento estratto dall'OBJ misura circa **2234 × 1439 mm**, quote geometriche provvisorie.
- Per un disco Coleman è stato riportato **Ø 60″ = 1524 mm**; il modello OBJ precedente mostra circa **1953 mm**. **Blocco tecnico:** verificare che la quota documentata si riferisca allo stesso allestimento e rivedere la scala prima di qualsiasi taglio. Non applicare un ridimensionamento uniforme indiscriminato.

## Archivio risorse e politica di pubblicazione

Il catalogo completo delle **142 risorse collegate** in questa fase del progetto è in [ARCHIVIO_RISORSE](docs/ARCHIVIO_RISORSE.md). Contiene i link Drive per tutte le versioni fino alla **REV14**, inclusi i PDF singoli, le tavole e gli ZIP precedenti.

**Non caricare file `.obj` nel repository**: GitHub conserva soltanto documentazione, tabelle, link e cronologia. Gli eventuali OBJ esistenti restano esclusivamente negli archivi Drive, chiaramente segnalati. Il file [`.gitignore`](.gitignore) esclude OBJ e ZIP da successivi commit locali.

I PDF e le dime DXF attuali sono **riferimenti di studio/preventivo**, non piani esecutivi CNC validati. **I file Drive sono privati:** il link non li rende pubblicamente accessibili.

## Fonti primarie di lavoro

La bibliografia aggiornata con i collegamenti verificati è in [FONTI.md](docs/FONTI.md).


- Disegno Perrotta/Coleman: *Revised Time Machine Drawings 7-19* (tavola fornita per il progetto).
- [Don Coleman, Time Machine Build 2025](https://colemanzone.com/Time_Machine_Project/Time%20Machine%20Build%202025/Time%20Machine%20Build%201.htm).
- Modello geometrico OBJ originale dell'archivio di progetto; da validare contro le quote documentate.

Il repository raccoglie **avanzamento, decisioni, criticità e specifiche**, mentre gli esecutivi restano soggetti a revisione tecnica.
