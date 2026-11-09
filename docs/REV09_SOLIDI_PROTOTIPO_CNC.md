# REV09 | Piedi in legno CNC: prototipi solidi con vani dimostrativi

**Data:** 2026-11-09 · **Stato:** PROTOTIPO GEOMETRICO, NON ESECUTIVO, NON CAM.  
**Oggetto:** 4 piedi ornamentali, 2 semigusci per piede, componenti estetici **NON PORTANTI**.

Questa revisione prosegue la [REV08](REV08_PIEDI_LEGNO_CNC.md). Le superfici aperte sono state convertite in **otto STL manifold chiusi**, ciascuno un singolo componente. **Il controllo `watertight` è un test geometrico, non certifica accuratezza cinematografica, resistenza del legno né lavorabilità CNC.**

## Link verificati ai file su Google Drive (privati)

| Risorsa | Collegamento | Contenuto |
| --- | --- | --- |
| **Pacchetto REV09 completo** | [ZIP, 26 file, circa 4,13 MB](https://drive.google.com/file/d/103bi5G24Y6h7gE_fsV2mbZub897Vfa-3/view?usp=drivesdk) | 4 STL sorgente non-manifold, 8 STL solidi, JSON parametri, script di rigenerazione, PDF, CSV, immagini, scheda artigiani e manifest |
| **Dossier tecnico** | [PDF A3, 9 tavole](https://drive.google.com/file/d/1HK34ki-zxgrP5MDG9h5KVsl2jkAHgeVw/view?usp=drivesdk) | Vista esplosa, sezione tasca, dati e condizioni per l'officina |
| **Parametri modificabili** | [JSON](https://drive.google.com/file/d/1XSEvCRhKcaqxR1pm4oaMOUHcxuEReD6b/view?usp=drivesdk) | Aperture di prova, passo voxel, sedi dei perni |
| **Script riproducibile** | [Python](https://drive.google.com/file/d/1FTZbPyT6xe5IrHBC4BSsKNeZ2rNmZw-j/view?usp=drivesdk) | Rigenera i solidi a partire dai 4 STL forniti nel ZIP; NON produce G-code |
| **Verifica degli 8 solidi** | [CSV](https://drive.google.com/file/d/1xh6BOT7bpkpRVtGL4xeDuvD8JalxvNTT/view?usp=drivesdk) | 8/8 `watertight=True`, 1 componente ciascuno |
| **Gate di approvazione** | [CSV](https://drive.google.com/file/d/1ZIjLHKj5wKdqwbRcVn01WJ2nbaUDNlui/view?usp=drivesdk) | 10 verifiche **aperte**, inclusi supporti veri, giunti e CAM |
| **Distinta del prototipo** | [CSV](https://drive.google.com/file/d/1IhZHvHBcxJMME87GZryUrrv6lDUeCHBx/view?usp=drivesdk) | Materiale e lavorazioni ancora da progettare |
| **Vista assemblata ed esplosa** | [PNG](https://drive.google.com/file/d/1Pff_x64PzxLoUkMrqkLyFIo34Y01TX2E/view?usp=drivesdk) | Due metà del piede P031 |

### Otto modelli solidi STL individuali (SOLO STUDIO)

| Piede | Semiguscio A | Semiguscio B |
| --- | --- | --- |
| P031 | [STL A](https://drive.google.com/file/d/1dgvVIwiFYF2kqQg3UTeOnecVc1C_AssI/view?usp=drivesdk) | [STL B](https://drive.google.com/file/d/1_reIlsjpEWOHSalqPuGENOqb1lxGbmnK/view?usp=drivesdk) |
| P032 | [STL A](https://drive.google.com/file/d/1q7PZ_Ce9ayps3KPi2tUcVTyh7xhzGcY0/view?usp=drivesdk) | [STL B](https://drive.google.com/file/d/18yKEwKC1mrL1kwMHMgMwB8YtcW01EmtZ/view?usp=drivesdk) |
| P033 | [STL A](https://drive.google.com/file/d/1bMqgwIxtQsydoiS1TEFCD31fZtme9c-O/view?usp=drivesdk) | [STL B](https://drive.google.com/file/d/1KCKP4PlJ42ZKWbSV_Du2IuHGvFEOu_dM/view?usp=drivesdk) |
| P034 | [STL A](https://drive.google.com/file/d/1WaM52cPcUkzsLxbZuFYXJjMALJaRPG35/view?usp=drivesdk) | [STL B](https://drive.google.com/file/d/10qRoSkhzExRPZhKFsNto3YigHbJ-6Olu/view?usp=drivesdk) |

## Cosa è stato realmente fatto

1. Recuperati i quattro STL delle geometrie P031-P034 dal precedente kit (non la fonte originale MGM). I file sorgente non erano manifold, con superfici non idonee come solidi.
2. Ricostruito un volume mediante voxelizzazione a **2,5 mm** e riempimento; la geometria esterna risulta quindi **approssimata, faccettata**.
3. Suddiviso ogni piede sul piano locale Y = **73,75 mm** in due metà A/B. Le metà sono chiuse, con un unico componente connesso ciascuna.
4. Creato **un vano INTERNO DI PROVA** tra X 115–180, Z 140–164 e profondità Y 23 mm per lato; NON rappresenta la piastra o il supporto reale.
5. Ricavate **due sedi cieche di centraggio per metà**, nominalmente Ø 10 × 15 mm, nei punti locali (X,Z) 65,158 e 215,158. **I perni di centraggio NON serrano i gusci**. Viti/staffe smontabili non modellate.
6. Validati con `trimesh` gli **8/8 solidi watertight** e l'assenza di componenti scollegati.
7. Preparati dossier e script che permette di modificare le dimensioni di prova. Il ZIP comprende i **quattro STL sorgente**, rendendolo rigenerabile senza usare file OBJ.

### Nota sulla scala

Il singolo piede sorgente P031–P034 occupava circa **302,35 × 143,90 × 180,06 mm** (classe G, ingombro del modello 1:1 precedente). La ricostruzione voxel REV09 porta il bounding box del pezzo assemblato a circa **305 × 147,5 × 182,5 mm**. **Non sostituisce il rilievo Perrotta/Coleman**, né costituisce un incremento dimensionale approvato.

## Da progettare con il carpentiere e il falegname

- [ ] Misure reali, forma e posizione dei supporti in acciaio/ruote; controllo delle zone di accesso.
- [ ] Vero scavo a misura; eventuale passaggio del supporto lungo il piede; spessori residui e orientamento fibre.
- [ ] **Bloccaggio meccanico smontabile** e accessibile (staffe/viti/inserto) senza trasferire carichi al guscio.
- [ ] Raffinamento delle superfici ornamentali sulle foto cinematografiche e delle sottosquadre.
- [ ] Prototipo economico delle due metà e controllo sull'acciaio reale; CAM fronte/retro e staffaggi.
- [ ] Verifica carichi e stabilità dell'intera macchina ([issue #6](https://github.com/HGWells2001/time-machine-project/issues/6)).

## Fonti e distinzione dal metodo Coleman

Don Coleman, [**The Feet, Build 2025**](https://colemanzone.com/Time_Machine_Project/Time%20Machine%20Build%202025/Time%20Machine%20Build%205.htm): gusci decorativi separati dai supporti in acciaio. **La costruzione in legno con CNC e i vani dimostrativi sono varianti nostre**, NON quote o procedure effettivamente documentate da Coleman.

Il modello precedente resta nella categoria geometria derivata (G) finché la scala del prop MGM non è stata convalidata ([issue #1](https://github.com/HGWells2001/time-machine-project/issues/1)). Nessun OBJ è stato caricato nel repository o nel ZIP REV09. I collegamenti Drive restano privati e non ne cambiano i permessi.

**Stato finale REV09:** 8 solidi geometrici DEMO chiusi, dossier e sistema riproducibile, ma **non approvati per produzione CNC o uso meccanico**.
