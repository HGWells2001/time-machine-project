# REV10 | Rilievo supporti e scassi parametrici per i piedi CNC

**Data:** 10 novembre 2026 · **Stato:** studio parametrico e kit di rilievo, **NON progetto esecutivo o CAM**.

La REV10 continua la [REV09](REV09_SOLIDI_PROTOTIPO_CNC.md), nella quale gli otto gusci di prova erano stati chiusi geometricamente ma mancavano i dati della vera carpenteria. Il nuovo criterio è **misurare prima il supporto in acciaio e l'inviluppo della ruota**, poi ricavare i vani e il fissaggio del legno. I gusci ornamentali restano **non portanti**.

## Collegamenti verificati a Google Drive (privato)

| Risorsa | Collegamento | Stato |
| --- | --- | --- |
| **Pacchetto completo REV10** | [ZIP, 34 file, 3,76 MB](https://drive.google.com/file/d/1tkFjJFvO99LrJFzBHJVG8PzBXXq-d0AN/view?usp=drivesdk) | 4 STL sorgente, 8 STL demo chiusi, 8 STEP dimostrativi, script, JSON, PDF, CSV, PNG e manifest SHA256. **Nessun OBJ**. |
| **Tavole A3** | [PDF, 8 pagine](https://drive.google.com/file/d/1h3jFYVaEiy5kqqMchuvNJc-V4MuLn2Fy/view?usp=drivesdk) | Rilievo, pianta, sezione, interferenze, procedura di officina e gate |
| **Configurazione da compilare** | [JSON con valori null](https://drive.google.com/file/d/12-zwKOjZ9kkdrBlROH2wXezTwg6GFRLk/view?usp=drivesdk) | Richiede misure vere dei quattro supporti |
| **Esempio dichiaratamente fittizio** | [JSON DEMO](https://drive.google.com/file/d/1dGcj3l717549S5RB6oclpkaTJjn5a8xy/view?usp=drivesdk) | Quote inventate per collaudo software: NON MGM / NON Coleman |
| **Generatore Python** | [genera_rev10.py](https://drive.google.com/file/d/1QhQCvMo-HpO3HBapWLMf0JILWC9seDfd/view?usp=drivesdk) | Genera studio STL/STEP, **non** G-code |
| **Modulo di rilievo** | [CSV, 48 valori da misurare](https://drive.google.com/file/d/1Ya0tXkYlRYOusttgd4gzyT2WR4wPMvmJ/view?usp=drivesdk) | Acciaio statico e ruota in movimento, per ciascun piede |
| **Gate di controllo** | [CSV G0-G8](https://drive.google.com/file/d/1q0hMSbAiPOvy0WcPKAqLLbvEAMi4BU5Y/view?usp=drivesdk) | 9 verifiche, **tutte aperte** |
| **Anteprima** | [PNG P031 con ingombri demo](https://drive.google.com/file/d/1QoO2vSfFoUL7A_rHyOktUq_6lRfuAwJ5/view?usp=drivesdk) | Supporto/ruota colorati = **fittizi** |
| **STEP acciaio, solo demo** | [P031 STEEL PLACEHOLDER](https://drive.google.com/file/d/1Yq32eLU9_6xUJ4sjPOkK4QKlePV5JLtc/view?usp=drivesdk) | Volume rettangolare inventato, non carpenteria |
| **STEP volume di scavo, solo demo** | [P031 CUT ENVELOPE](https://drive.google.com/file/d/1FTfdpk8piNAwo5A4vaCVQLKa5JtH_irP/view?usp=drivesdk) | Gioco fittizio e bounding box, non vera cavità |
| **STL P031-A, solo demo** | [P031 A](https://drive.google.com/file/d/1CvjMWrOh1TCQbWZi3CVnzEC8rE-M8q4g/view?usp=drivesdk) | Guscio voxelizzato chiuso, non CNC |
| **STL P031-B, solo demo** | [P031 B](https://drive.google.com/file/d/1dnixlbdz_fQcKz2DuokPLy83w9VBUpd-/view?usp=drivesdk) | Guscio voxelizzato chiuso, non CNC |

**Tutti i 34 membri dello ZIP sono individuabili attraverso il pacchetto e il manifest SHA256 interno.** Tra questi ci sono anche gli altri 6 STL demo e 6 STEP relativi a P032–P034. I file Drive sono rimasti privati.

## Fonti e provenienza

- **D:** [Don Coleman, *The Feet*, Build 2025](https://colemanzone.com/Time_Machine_Project/Time%20Machine%20Build%202025/Time%20Machine%20Build%205.htm). Coleman documenta quattro supporti in acciaio con ruote, gusci estetici in due parti, adattamento manuale e stampi in silicone per la resina. **Non fornisce quote tecniche delle staffe e dei castor utilizzabili per fresare i nostri gusci**.
- **G:** mesh piedi P031-P034 del vecchio kit, classe geometrica, ingombro di riferimento circa **302,35 × 143,90 × 180,06 mm**. La calibrazione originale 1:1 resta da convalidare.
- **I:** intero modello DEMO di staffa, ruota, margine di gioco e scavo. I valori del JSON dimostrativo **sono inventati**.
- **V:** misure effettive del supporto, ingombro dinamico della ruota, accesso al freno, viti, lamierati, parete residua in legno e stabilità.

## Test completati

- [x] Il generatore legge i quattro STL sorgente in mm e li converte a voxel da 2,5 mm per studio, senza utilizzare il file OBJ.
- [x] Con l'input reale originale contenente `null`, **interrompe intenzionalmente la generazione** prima di produrre output.
- [x] Con `--demo` esplicito produce **8 STL chiusi e monocomponente** (4 piedi × 2 metà), più **8 STEP** dei volumi di supporto/scavo.
- [x] ZIP verificato integro, 34 file, zero OBJ e zero G-code. SHA256: `14261697e1ee5f2de511c629e9804ae49ca8544ffda7bb3d25b5d48c094b8d5b`.
- [x] PDF A3 a 8 pagine renderizzato e verificato.

## Uso del generatore

```bash
python 01_CONFIGURAZIONE_E_SCRIPT/genera_rev10.py --demo
# utilizza SOLTANTO le quote inventate in ESEMPIO_FITTIZIO_NON_REALE.json
```

Per i rilievi effettivi, compilare `RILIEVI_REALI_DA_COMPILARE.json` con acciaio statico e ingombro della ruota in movimento per **ogni** supporto. Il margine di gioco deve essere deciso dall'officina. Anche con rilievi reali, lo script genera solo **volumi approssimati a box**, non un profilo effettivo del supporto né modelli approvati per la produzione.

**Non sono modellati:** fori, incastri, viti, staffe di ritenuta, spessori finali, CAD decorativo di dettaglio o utensili CAM. Gli STEP sono *volumi ausiliari*, non STEP esecutivi dei gusci.

## Lavorazioni ancora aperte

- [ ] Carpentiere: realizzare o fornire un rilievo preciso dei quattro supporti e del campo di movimento delle ruote.
- [ ] Tecnico: verificare carichi, stabilità, punti di fissaggio e disposizione reale delle ruote ([#6](https://github.com/HGWells2001/time-machine-project/issues/6)).
- [ ] Falegname/CAD: sostituire i box con il profilo preciso del supporto, progettare il guscio e misurare le pareti residue.
- [ ] Falegname/carpentiere: scegliere e dimensionare il **serraggio smontabile**. Le sedi demo della REV09 non assicurano tenuta.
- [ ] CNC: setup fronte/retro, utensili, sottosquadri, prova su materiale economico.
- [ ] Direzione artistica: fedeltà ai rilievi MGM rispetto a Perrotta/Coleman prima della produzione.

Collegamenti: [REV08 superfici](REV08_PIEDI_LEGNO_CNC.md) · [REV09 prototipi chiusi](REV09_SOLIDI_PROTOTIPO_CNC.md) · [REV07 carpenteria](REV07_TELAIO_PIEDI.md). **Nessun OBJ pubblicato su GitHub.**
