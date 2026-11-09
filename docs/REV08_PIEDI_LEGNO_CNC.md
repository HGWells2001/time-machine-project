# REV08 | Quattro piedi ornamentali in legno, fresatura CNC

**Data:** 9 novembre 2026 · **Stato:** studio CAD/CAM preliminare. **Non è pronto per CNC, non contiene G-code, fori, scavi, giunti o solidi chiusi.**

Questa revisione segue la scelta di **sostituire gli 8 semigusci decorativi in resina con 8 semigusci in legno lavorabili da un falegname CNC**. La struttura interna in acciaio con ruote resta portante e indipendente. L'idea dei gusci su una struttura metallica riprende la separazione dei ruoli documentata da Don Coleman, ma **Coleman non utilizza CNC in legno per questi piedi nella pagina citata**.

## I file prodotti e verificati su Google Drive

| Risorsa | Link | Stato |
| --- | --- | --- |
| **Pacchetto REV08, 23 file** | [ZIP completo](https://drive.google.com/file/d/1ecdclIXV0Ws0Q1FsSOXR9kwvF_wlfCpC/view?usp=drivesdk) | Contiene 8 STL di superfici APERTE, PDF 11 tavole A3, DXF, CSV/JSON, schemi, manuale e verifiche; **zero OBJ** |
| **Tavole tecniche illustrate, 11 pagine** | [PDF A3](https://drive.google.com/file/d/1udbiZIESlwbwog-1dxQ7hlpWje-E5zRA/view?usp=drivesdk) | Preventivo preliminare, non esecutivo |
| **Sagome laterali XZ e piante XY** | [DXF in mm](https://drive.google.com/file/d/1ocefri311QlB8QuZGsBckowxlK5HJpTU/view?usp=drivesdk) | **NON CNC**: profili proiettati, nessun percorso utensile |
| **Dimensioni 8 semigusci** | [CSV](https://drive.google.com/file/d/1brUZ-aXOO8cb46VPJ0nt6jcogrik3HTK/view?usp=drivesdk) | Misure geometriche classe G |
| **Verifica simmetrie** | [CSV](https://drive.google.com/file/d/1SeTuMvzOo7Gt15-Q7t-wG_zXCvG4VH7T/view?usp=drivesdk) | Riconoscimento famiglie speculari |
| **Gate per la lavorazione CNC** | [CSV](https://drive.google.com/file/d/1g5MQJSJcAT7DJhbTMdvyvvW07JdAKEtV/view?usp=drivesdk) | G0-G8, tutti aperti |
| **Distinta di preventivo** | [CSV](https://drive.google.com/file/d/1ECW271GSZeFA7mTrvq-UlW9LV-c5euP5/view?usp=drivesdk) | Fasi CAD, prototipo, produzione |
| **Metadati della geometria** | [JSON](https://drive.google.com/file/d/1kK9g_HiTPJj1vTMkvUsqjxdzd7-7trz-/view?usp=drivesdk) | Origine OBJ precedente, non ripubblicato |
| **Anteprima piede intero e aperto** | [PNG](https://drive.google.com/file/d/1gAAV2Mv0ydKuwM5AA7_GPRKjlz5Q_K4I/view?usp=drivesdk) | Confronto visivo |
| **Quattro sagome laterali** | [PNG](https://drive.google.com/file/d/1Bov32dbIkdb6IRm3toPuEihE4f0pHjsZ/view?usp=drivesdk) | Silhouette tecniche |

### Otto STL individuali: superfici esterne, non solidi

| Piede | Semiguscio Y- | Semiguscio Y+ |
| --- | --- | --- |
| **P031** | [P031-A](https://drive.google.com/file/d/1pPUSSRcoY4fhcTcJ7YIMYHxQPzU3xfsF/view?usp=drivesdk) | [P031-B](https://drive.google.com/file/d/1egnsDGmndI02RaRUmfacvXaPkyJtCJ2Q/view?usp=drivesdk) |
| **P032** | [P032-A](https://drive.google.com/file/d/1XSs4DvcSWeUBK4dtGRTcTUnXLwj7xmsf/view?usp=drivesdk) | [P032-B](https://drive.google.com/file/d/1j6BOVDIW_6fSkRidle95fpAAdNx1lbAY/view?usp=drivesdk) |
| **P033** | [P033-A](https://drive.google.com/file/d/1OBh5XJ5z8a4cOiwoKhJm2pkNqM416XCM/view?usp=drivesdk) | [P033-B](https://drive.google.com/file/d/1jVz_Q6Wu9PNaMT7YICRH4UMdBjCxCbyX/view?usp=drivesdk) |
| **P034** | [P034-A](https://drive.google.com/file/d/1KGcqEAcSHPMKSfLP0knv2ujbaZaDemth/view?usp=drivesdk) | [P034-B](https://drive.google.com/file/d/15urBddFt_AG5lWHDnuic29YPASMXtfIT/view?usp=drivesdk) |

I collegamenti Drive **sono privati**; la loro presenza nel repository pubblico non modifica i permessi. Gli STL sono conservati soltanto su Drive. **Nessun file OBJ è stato caricato su GitHub.**

## Risultato verificato della separazione

Ho usato gli STL P031-P034 del precedente kit 75 parti, derivati da un modello OBJ 1:1 **non ancora confrontato definitivamente con le quote originali Perrotta/Coleman**.

| Valore | mm | in circa | Classe |
| --- | ---: | ---: | --- |
| Singolo piede, X lungo | **302,35** | 11,90 | G |
| Singolo piede, Y trasversale | **143,90** | 5,67 | G |
| Singolo piede, Z verticale | **180,06** | 7,09 | G |
| Singola metà, ingombro Y | **71,95** | 2,83 | G |
| Piano di separazione locale | **Y = 71,95** | 2,83 | I su geometria G |
| Ogni mesh originale | **460 triangoli** | | G |
| Ogni semiguscio aperto | **312 triangoli** | | Derivato |

Le metà risultano **aperte e non watertight**, dunque non hanno volume, cavità o spessore. La mesh presenta poche facce per descrivere un piede ornamentale: non riproduce ancora la qualità dei dettagli scolpiti che si vedono nelle fotografie del prop.

### Simmetrie e vantaggio economico

- P031 e P034 risultano identici entro la precisione della mesh.
- P032 e P033 risultano identici entro la precisione della mesh.
- Coppie anteriore e posteriore sono speculari in X.
- Le metà A e B di ogni piede sono speculari in Y.

Si può valutare **un insieme ridotto di geometrie master** con istanze speculari e otto identificativi di montaggio. Il falegname deve comunque verificare il ribaltamento sul CAM, il verso vena e lo staffaggio prima di riusare un percorso utensile.

## Come trasformarli in pezzi CNC veri

1. Confermare la scala 1:1 e rilevare il supporto portante reale in acciaio, ruota e ingombri ([#1](https://github.com/HGWells2001/time-machine-project/issues/1), [#6](https://github.com/HGWells2001/time-machine-project/issues/6)).
2. Ricostruire in CAD le superfici, i rilievi e i sottosquadri dalle foto originali e dai disegni. L'attuale STL è troppo sommario per il dettaglio definitivo.
3. Modellare **solidi chiusi** dei due semigusci con cavità interna su misura, spessore residuo, linea di giunzione, eventuali spine e viti nascoste.
4. Scegliere legno e grezzo. Un **possibile volume iniziale** di riferimento è 330 × 100 × 210 mm per mezzo piede, **non è un ordine di materiale o una quota esecutiva**.
5. Eseguire simulazione CAM fronte/retro con riferimenti di riposizionamento, misurare sottosquadri, definire fresa e staffaggi. Il CAM della CNC a 3 assi è responsabilità dell'officina.
6. Fresare una coppia campione, montarla a secco sul supporto reale e verificare giunti, raggi utensile, accesso ruote e finitura. Approvare il campione prima della serie di altri tre piedi.

La **finitura legno** va campionata per imitare l'aspetto originale. Coleman descrive red mahogany stain e shellac per il basamento in legno; sul suo piede di resina usa trattamento estetico diverso. Non trasformare automaticamente quel processo in una prescrizione per questo legno.

## Fonti e limiti

- [Don Coleman, **The Feet** (2025)](https://colemanzone.com/Time_Machine_Project/Time%20Machine%20Build%202025/Time%20Machine%20Build%205.htm): gusci in due metà, master, silicone, resina e supporti in acciaio per ruote. **La CNC in legno è una nostra variante.**
- [Don Coleman, **The Base** (2025)](https://colemanzone.com/Time_Machine_Project/Time%20Machine%20Build%202025/Time%20Machine%20Build%201.htm): falegnameria della base stratificata, distinta dai piedi.
- [Wood Magazine, fresatura su due lati](https://www.woodmagazine.com/tool-reviews/cnc-machines/look-at-cnc-from-both-sides-now): necessità di un sistema di registrazione dei grezzi durante il ribaltamento.
- [REV07 su GitHub](REV07_TELAIO_PIEDI.md): coordinate dei piedi classificati G, limiti di portata, struttura e supporti da progettare.

**Stato: REV08 completata come consegna di studio e preventivo. Non autorizza fresatura di produzione né la seduta di una persona sulla macchina.**
