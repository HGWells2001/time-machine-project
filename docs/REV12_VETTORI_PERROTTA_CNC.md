# REV12 | Curve vettoriali originali dal blueprint Perrotta/Coleman

**Data:** 10 novembre 2026. **Scopo:** replica artigianale 1:1 di _The Time Machine_ (George Pal, MGM, 1960). **Stato:** rilievo grafico vettoriale, NON CNC e NON esecutivo.

Questa revisione **non scala l'OBJ precedente**. Estrae invece direttamente dal PDF sorgente le curve vettoriali dei due ornamenti sotto il basamento in vista laterale e dei quattro profili visibili sotto il basamento in vista frontale. È il primo materiale CAD 2D derivato dalle **curve di Bézier della tavola**, non da un suo screenshot o dalla mesh 3D grossolana.

## Risorse verificate in Google Drive privato

| ID | Tipo | Contenuto | Link |
| --- | --- | --- | --- |
| **R101** | ZIP completo, **24 file** | Sei DXF mm, sei SVG, PDF A3, due script, registri e anteprime. SHA256 `f1240578aa480e70a079939c4b5419abae843504938a71a87d49c867e94fb88e`. **Zero OBJ**. | [REV12 pacchetto completo](https://drive.google.com/file/d/1dp2DvruKjpKPZ7HvGi2h0ews065xo9Jd/view?usp=drivesdk) |
| **R102** | PDF A3, **6 tavole** | Quattro tavole con proiezioni in scala nominale 1:1, una introduttiva e una di validazione; barra da 50 mm per controllare la stampa. | [REV12 dossier A3](https://drive.google.com/file/d/1CHX0RKjk-1GmqRE4hG9-k8Fq-jlnjQxs/view?usp=drivesdk) |
| R103 | DXF | Riccio laterale sinistro, **51 tracciati** separati, polilinee di sola lettura. | [Lato sinistro](https://drive.google.com/file/d/1sstIPmzQ0yZmRs3rCtPz-VdtNWNWJ77R/view?usp=drivesdk) |
| R104 | DXF | Riccio laterale destro, **51 tracciati** separati. | [Lato destro](https://drive.google.com/file/d/1037NoAYjTSiX39kcJE_d2p4mNzg9_bvd/view?usp=drivesdk) |
| R105 | DXF | Sostegno frontale F1, 10 tracciati. | [Frontale F1](https://drive.google.com/file/d/1u7vCClfWEU1c68_MxpJTB8Zlm0m3zwnd/view?usp=drivesdk) |
| R106 | DXF | Sostegno frontale F2, 12 tracciati. | [Frontale F2](https://drive.google.com/file/d/1lXoWM-1OaseqUvfypHHIARIu9fgf2d7E/view?usp=drivesdk) |
| R107 | DXF | Sostegno frontale F3, 12 tracciati. | [Frontale F3](https://drive.google.com/file/d/12H5dQOVgFqMbyyehrFKapeL4qhfaVpPT/view?usp=drivesdk) |
| R108 | DXF | Sostegno frontale F4, 10 tracciati. | [Frontale F4](https://drive.google.com/file/d/1DajZ97klckgE6sIA1c8qCmZJEfHZqyF_/view?usp=drivesdk) |
| R109 | CSV | Coordinate e misure 6 proiezioni con classi G-Perrotta. | [Registro quote vettoriali](https://drive.google.com/file/d/1pFjFiSLD3ueJU1NraSWP4CmFtTsQ0Ac1/view?usp=drivesdk) |
| R110 | PY | Estrattore riutilizzabile da PDF sorgente, per rigenerare i DXF/SVG senza OBJ. | [Script Python](https://drive.google.com/file/d/1fSST7ubFWup0g3aTj68TB9rRAHPMrr8U/view?usp=drivesdk) |
| R111 | PNG | Panoramica dei sei profili. | [Anteprima REV12](https://drive.google.com/file/d/1VQeNYix2v8-SiQ-YmR13tt6Y10v40JyB/view?usp=drivesdk) |

Tutti i link sono stati letti e verificati tramite Google Drive; **i permessi sono privati**. Dentro lo ZIP sono presenti anche sei SVG, le immagini delle tavole e i registri di confronto. **Né il PDF originale completo Perrotta/Coleman, né i tracciati vettoriali estratti sono caricati nel repository GitHub pubblico.** Per ragioni di copyright rimangono nel Drive privato.

## Calibrazione verificata sul righello del PDF sorgente

La tavola di Chris Perrotta, revisionata da Don Coleman, contiene un **righello grafico 0–12 pollici**, corrispondente a 304,8 mm.

- Posizione dei segni principali `0` e `12` nella rasterizzazione del PDF a **4×**: pixel circa **43,5** e **390**, distanza **346,5 px**.
- Distanza nel sistema grafico del PDF: **86,625 punti**, quindi **3,518615 mm per punto PDF**.
- Il valore deriva dalla stampa grafica, **non da una quota numerica** fornita dall'autore per il singolo piede.
- Le DXF e SVG conservano in millimetri i tracciati, ma la sorgente e i campioni impongono **incertezza dimensionale prudenziale di circa ±15 mm** sugli ingombri reali; le cifre decimali sono utili per ricostruire il vettore, non certificazioni metrologiche.

## Misure ricavate direttamente dai tracciati

| Proiezione | Larghezza nel disegno (mm) | Altezza nel disegno (mm) | Tracciati | Identità |
| --- | ---: | ---: | ---: | --- |
| Riccio ornamentale laterale sinistro | **246,3** | **155,8** | 51 | Curva esterna visibile sotto il basamento |
| Riccio ornamentale laterale destro | **249,3** | **155,9** | 51 | Curva esterna speculare in vista laterale |
| Sostegno frontale F1 | **126,4** | **133,8** | 10 | Profilo frontale, senza interno |
| Sostegno frontale F2 | **126,5** | **133,8** | 12 | Profilo frontale, senza interno |
| Sostegno frontale F3 | **126,5** | **133,8** | 12 | Profilo frontale, senza interno |
| Sostegno frontale F4 | **126,5** | **133,8** | 10 | Profilo frontale, senza interno |

**Nuova distinzione decisiva:** la vista laterale mostra **due ricci ornamentali** e la vista frontale mostra **quattro profili di sostegno**; **non è stato dimostrato che costituiscano quattro solidi 3D ottenibili semplicemente unendo queste sagome**. Per questo i file sono identificati `LATO_SINISTRO`, `LATO_DESTRO`, `FRONTE_1…4`, non rinominati arbitrariamente P031…P034. Questa cautela evita di fresare un piede fisicamente scorretto.

### Confronto con la REV11A e il vecchio OBJ

La [REV11A](REV11A_QUOTE_PERROTTA.md) proponeva stime di insieme **250 × 135 × 150 mm ±15**, coerenti grossolanamente con la nuova lettura, ma con **proiezioni mescolate**. REV12 separa e riporta i valori effettivamente disegnati. Il vecchio OBJ attribuiva a P031-P034 un box di circa **302 × 144 × 180 mm** e **non è stato usato né deformato** per costruire i DXF.

La [REV11](REV11_RILIEVO_OFFICINA_CNC.md) richiede 48 misure del supporto reale e del movimento ruote. **Queste quote restano vuote**: il blueprint mostra l'esterno, non sezioni interne portanti, staffe, bulloni o caster in tutte le posizioni.

## Ricalcolo REV13 degli estremi dei vertici DXF

La [REV13](REV13_RILIEVI_2_5D.md), usando gli stessi sei DXF come ingresso, misura nei punti LWPOLYLINE **242,914 mm (SX)** e **243,474 mm (DX)**, contro **246,317 / 249,262 mm** del registro di quote vettoriali REV12. Si tratta di una **discordanza di metodo ancora aperta** pari a circa 3,403 e 5,788 mm. Non correggere la scala, attribuire i numeri all'originale MGM o usare gli ingombri come quote CNC finché la divergenza non è spiegata. Gli altri frontali risultano sostanzialmente coincidenti.

## Validazioni effettuate

- [x] Estratte **6 proiezioni** dalla pagina PDF vettoriale originale.
- [x] Convertite le curve in **6 DXF R2010 con unità millimetri** (`$INSUNITS=4`) e **6 SVG**.
- [x] Verificato ogni DXF con parser indipendente: **51+51+10+12+12+10 polilinee**.
- [x] Creato PDF di 6 pagine A3 e controllato il rendering delle tavole.
- [x] Archivio ZIP testato integro, 24 file, zero OBJ.
- [x] Generatore Python incluso per riprodurre il risultato **solo avendo il PDF legittimamente disponibile**.

### Cosa manca per la CNC e per la struttura

1. Verifica dell'identificazione delle parti tra le viste e fotografie, con ricostruzione 3D dei rilievi.
2. Definizione degli **spessori dei gusci** e della linea di apertura intorno alla struttura d'acciaio.
3. Rilievo o progetto verificato delle **quattro staffe portanti e delle ruote**, inclusi freni/accessibilità.
4. Progettazione dei giunti nascosti e verifica dei carichi. I gusci devono restare non portanti.
5. Solo allora solido CAD, CAM fronte/retro con utensili e macchine reali, e prototipo di prova.

Nessuna curva REV12 è un percorso utensile o un contorno chiuso per fresare. Gli originali Perrotta/Coleman sono materiale protetto; il repo pubblica **il metodo e i link**, non il disegno vettoriale.

Documenti correlati: [fonti](FONTI.md) · [REV11A](REV11A_QUOTE_PERROTTA.md) · [REV11](REV11_RILIEVO_OFFICINA_CNC.md) · [REV08 superfici](REV08_PIEDI_LEGNO_CNC.md) · [REV09 prototipi](REV09_SOLIDI_PROTOTIPO_CNC.md).
