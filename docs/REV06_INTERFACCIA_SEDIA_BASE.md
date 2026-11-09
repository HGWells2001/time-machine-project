# REV06 | Collegamento della sedia Berninghaus al basamento

**Data:** 2026-11-09. **Stato:** studio di interfaccia / pre-progettazione, **NON esecutivo e NON CNC**. È una replica artigianale con falegnami e carpentieri, non un progetto per stampa 3D.

## Documenti REV06 archiviati su Google Drive (tutti privati)

| Tipo | Risorsa |
| --- | --- |
| **ZIP completo, 12 file** | [REV06 interfaccia sedia/base](https://drive.google.com/file/d/1nMBo4vrMrQ60BUlX-t8cCCC2sY1N8tcW/view?usp=drivesdk) |
| **PDF A3, 10 tavole** | [Dossier con planimetria e sezione](https://drive.google.com/file/d/1v1K1_i2EWOETDP0WCGOOXZKOGf6OsKL8/view?usp=drivesdk) |
| **DXF non CNC** | [Sovrapposizione di ingombri P035/P018 e piedi](https://drive.google.com/file/d/1Eq75DvpiTiQAbL9-ZVDgZYMiiwLBf_Wj/view?usp=drivesdk) |
| **CSV misure** | [Registro interfaccia e provenienza](https://drive.google.com/file/d/1wa7bL-H6HMmfshDTkyp-R0bLkJHmWf8A/view?usp=drivesdk) |
| **CSV avanzamento** | [Blocchi e requisiti per la fabbricazione](https://drive.google.com/file/d/1dxjtK-TlqId1dUyfekSItFxpCoYMffO1/view?usp=drivesdk) |
| **JSON coordinate** | [Dati macchina derivati dall'archivio OBJ](https://drive.google.com/file/d/1KFg2dfjhDANMs_xKb02cxtA_Yvzd6rWS/view?usp=drivesdk) |
| **Scheda artigiani** | [Responsabilità e rilievi necessari](https://drive.google.com/file/d/1sSIbMQ5TN_8cGaEfqr8YKVejcnd_Qrn-/view?usp=drivesdk) |
| **Anteprima PNG** | [Sovrapposizione in pianta](https://drive.google.com/file/d/1FtroPkREd4HLSCUCA_-Ih6VfgffRHpUX/view?usp=drivesdk) |

Il PDF è composto da 10 pagine: copertina, fonti, pianta, sezione verticale, fissaggio storico, percorso carichi, alternative, sequenza di lavorazione, registro misure e consegne per artigiani.

## Il dato storico nuovo, documentato da Chris Perrotta

[Perrotta, «The Time Machine chair»](https://erkelzaar.tsudao.com/models/perrotta/TM_chair.htm): nella sedia MGM il piedistallo della poltrona da barbiere era stato **rimosso**; il fondo reca impronte di **quattro gambe aggiunte** e **due fori** usati per aste metalliche di ritenuta verso il basamento, una zona anteriore e una posteriore. Queste fotografie **non** forniscono interassi e diametri attendibili. Non si può assumere che due aste storiche, da sole, rendano sicura una replica su cui sedersi.

Il riferimento funzionale di Coleman resta [The Chair, 2025](https://colemanzone.com/Time_Machine_Project/Time%20Machine%20Build%202025/Time%20Machine%20Build%202.htm); per il supporto si usa anche [The Base, 2025](https://colemanzone.com/Time_Machine_Project/Time%20Machine%20Build%202025/Time%20Machine%20Build%201.htm) e [The Feet, 2025](https://colemanzone.com/Time_Machine_Project/Time%20Machine%20Build%202025/Time%20Machine%20Build%205.htm).

## Sovrapposizione geometrica di studio (classe G)

**Non è una revisione della calibrazione:** i numeri vengono dal catalogo del vecchio kit da 75 parti, basato sull'OBJ 1:1 **non ancora validato** con le quote originali Perrotta/Coleman. X = lunghezza (positivo verso console), Y = lato, Z = altezza, mm.

| Riferimento | Misura | Fonte |
| --- | --- | --- |
| P035, basamento | box X **2233,87 mm**, Y **1439,48 mm** | Catalogo 75 parti, REV03 |
| P018, cuscino/seduta | box X **767,55 mm**, Y **597,39 mm** | Catalogo 75 parti, REV03 |
| Centro P018 rispetto al centro P035 | **+153,84 mm X**, Y circa 0 | Calcolo dai box del catalogo |
| Z superiore del basamento P035 | **278,27 mm** | Catalogo 75 parti |
| Z inferiore/superiore seduta P018 | **632,82 / 750,78 mm** | Catalogo 75 parti |
| Piano superiore seduta - piano base | **472,51 mm (18,60″)** | Differenza quote G |
| Spazio fino al volume inferiore seduta | **354,55 mm (13,96″)** | Differenza quote G |

**Non usare** i riquadri, il punto centrale o i quattro piedi P031-P034 come sagome di taglio, centri di foratura o interassi di ancoraggio. Il DXF presenta soltanto bounding box con layer «NON CNC», assi e testo di avviso. Nessun percorso utensile, nessun foro.

La tavola indipendente della sedia, analizzata nella [REV05](REV05_SEDIA_BERNINGHAUS.md), dava un ingombro grafico orientativo di circa 670 × 750 × 900 mm, con incertezza cautelativa ±25 mm: non va confuso con il solo riquadro del cuscino P018.

## Percorso dei carichi: proposta da valutare

**Occupante → telaio resistente della sedia → adattatore smontabile → telaio metallico interno da progettare → quattro supporti portanti con ruote → pavimento.**

È una **proposta architetturale**, non un dimensionamento. Il legno con 4 strati Coleman e la resina dei gusci hanno valore scenografico e possono essere strutturali solo se appositamente progettati e verificati. Scelta provvisoria per studio: telaio portante nascosto indipendente dalle modanature.

### Mancano per autorizzare la costruzione
- [ ] Validazione della scala generale, soprattutto il disco posteriore ([issue #1](https://github.com/HGWells2001/time-machine-project/issues/1)).
- [ ] Rilievo reale dell'impronta sotto la sedia e dei fissaggi, senza inventare fori dalle foto.
- [ ] Approvazione delle 4 dime e della base ([issue #2](https://github.com/HGWells2001/time-machine-project/issues/2)).
- [ ] Disegno di carpenteria con masse, baricentro, ruote, portata della seduta e ribaltamento ([issue #3](https://github.com/HGWells2001/time-machine-project/issues/3)).
- [ ] Mock-up a secco 1:1 e prova di accessibilità ai giunti.
- [ ] Revisione da parte di falegname e tecnico prima di tagliare, forare o saldare.

**Nessun OBJ viene pubblicato su GitHub o incluso nella REV06.** Il nuovo pacchetto contiene 12 file propri, con PDF/CSV/DXF/JSON/PNG/MD.
