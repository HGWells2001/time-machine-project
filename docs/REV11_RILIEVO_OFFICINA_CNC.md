# REV11 | Rilievo operativo dei piedi CNC e verifica interferenze

**Data:** 10 novembre 2026 · **Stato:** dossier di officina / pre-progettazione. **NON esecutivo e NON CNC.**

La scelta progettuale rimane: **otto semigusci decorativi in legno fresato CNC** montati attorno ai **quattro supporti portanti indipendenti in acciaio**, con ruote. La geometria dei supporti NON è ancora stata fornita; la presente revisione **non crea scassi o fori di produzione**.

## Deliverable e collegamenti verificati (Google Drive privato)

| Risorsa | Collegamento | Utilizzo |
| --- | --- | --- |
| **Pacchetto completo REV11** | [ZIP, 15 file](https://drive.google.com/file/d/1xyKjEVHAxjkSzhAjb14zGDf7NWhSgvUj/view?usp=drivesdk) | Dossier, quattro schede A4, template dati, validatore e anteprime |
| **Dossier REV11** | [PDF A3, 9 tavole](https://drive.google.com/file/d/1Z0zeEV6RiKhAImjzTz_fn0zTX4t3VRpF/view?usp=drivesdk) | XYZ, 48 quote, ruote e freni, giunto schematizzato, piano lavori e gate |
| **Schede individuali P031-P034** | [PDF A4, 4 schede](https://drive.google.com/file/d/1nj9JJQdUBarIUgBc2KI0FMv3LDhhOld0/view?usp=drivesdk) | Da stampare e compilare durante il rilievo fisico |
| **48 quote di rilievo** | [CSV vuoto](https://drive.google.com/file/d/1h8EoIuHukapx_SVAJBAeDAqbx8856ODe/view?usp=drivesdk) | 6 estremi acciaio + 6 estremi ruota per ciascuno dei quattro piedi |
| **Interferenze** | [CSV, 36 scenari](https://drive.google.com/file/d/1YFKZ9IrWOnoop3vFwWCUJPHVivxxjKZw/view?usp=drivesdk) | Orientamenti ruota 0/90/180/270, freno e manutenzione |
| **Montaggio/smontaggio** | [CSV, 40 attività](https://drive.google.com/file/d/14hkj8NGW0y4tZafPCYDSGiBWZZm0-qnm/view?usp=drivesdk) | Sequenza proposta, responsabili e prove a secco per P031-P034 |
| **Gate di approvazione** | [CSV, G00-G10](https://drive.google.com/file/d/1H33Fnmpse-pxeDhSIEIx-NB28XM2wBRC/view?usp=drivesdk) | Tutti aperti, nessuna autorizzazione a fresare |
| **Configurazione parametrica reale** | [JSON con null](https://drive.google.com/file/d/1r3FDXVxznVefqP4gPVohwmOCxS07faZK/view?usp=drivesdk) | Schema compatibile concettualmente con REV10, senza riempire quote fittizie |
| **Validatore delle misure** | [Python, solo controllo CSV](https://drive.google.com/file/d/1Nxe8UEAAzCRtFr3d-wyZGLXiFLtV7Yvs/view?usp=drivesdk) | Verifica completezza, min/max, conversioni, nome, data, strumento e stato MISURATA |
| **Panoramica A3** | [PNG](https://drive.google.com/file/d/1wqseriNKI6Vy-b1sqUanfiHO1hUZ5EE0/view?usp=drivesdk) | Anteprima delle nove tavole |

**Permessi Drive invariati:** i file sono privati. Sono soltanto collegati qui. **Nessun OBJ, STL o STEP aggiunto al repository**, nessun G-code generato.

## Metodo e provenienza: non confondere le fonti

| Categoria | Dato | Stato |
| --- | --- | --- |
| **D - documentato** | Don Coleman costruisce quattro supporti per ruote in acciaio tagliato waterjet e saldato; realizza gusci ornamentali separati, adattati alla carpenteria. | [The Feet (2025)](https://colemanzone.com/Time_Machine_Project/Time%20Machine%20Build%202025/Time%20Machine%20Build%205.htm) |
| **D - documentato** | Base di compensato stratificato, distinta dal guscio dei piedi. | [The Base (2025)](https://colemanzone.com/Time_Machine_Project/Time%20Machine%20Build%202025/Time%20Machine%20Build%201.htm) |
| **G - geometria derivata** | Box P031-P034 del modello precedente. | Riferimento VISIVO, non punti reali di ruote, staffe o fori |
| **I - ipotesi** | Semigusci in legno CNC, modulo A4, percorso di smontaggio, matrice interferenze, registrazione delle foto. | Soluzioni di progetto da convalidare |
| **V - da verificare** | Dimensioni di acciaio, caster, freni, supporti, viti, spessori e carichi. | Valori ancora mancanti |

La CNC in legno è **una nostra variante** rispetto ai gusci in resina di Coleman. Il sito NON fornisce le 48 quote richieste per l'acciaio.

## Misure necessarie

Per ciascuno dei quattro supporti, registrare gli estremi X_min/X_max, Y_min/Y_max e Z_min/Z_max per:
1. `ACCIAIO_STATICO` completo di bulloneria e attacchi;
2. `INVILUPPO_RUOTA_IN_MOVIMENTO` comprendendo sterzata, oscillazione e freno.

**48 valori mm** (4 piedi × 2 oggetti × 6 coordinate). Conversione: 1 in = 25,4 mm esatti; il valore in pollici può essere calcolato dopo la misura e non deve diventare nuova fonte di arrotondamento. Indicare **data ISO (YYYY-MM-DD), strumento, rilevatore e certezza MISURATA/RILEVATA**, non “DA_MISURARE”. La conferma dell'origine locale XYZ è obbligatoria come gate indipendente.

Non basta la bounding box: il progetto esecutivo richiederà anche il profilo effettivo del supporto con bulloni, accesso ai freni e sistema di ritenuta smontabile.

## Verifiche del validatore

Il file `verifica_rilievi_rev11.py` usa soltanto Python standard e non importa gli STL. Test effettuati:

- [x] CSV vuoto originario REV10 (0/48): restituisce `BLOCKED`, exit code **2**.
- [x] CSV sintetico **fittizio solo in memoria di prova** con 48 quote coerenti, date e rilevatori: restituisce `MEASUREMENTS_CONSISTENT_NOT_APPROVED`, exit code **0**.
- [x] CSV di prova con min/max o conversioni incoerenti: restituisce `BLOCKED`, exit code **2**.
- [x] ZIP verificato senza errori: **15 file**, non contiene OBJ, STL, STEP o G-code.
- [x] PDF A3 (9 pagine) e PDF A4 (4 pagine) renderizzati per controllo visivo.

Anche un CSV che passa il test **non chiude i gate**: il software controlla la consistenza dei campi, non la veridicità delle misure né la sicurezza della macchina.

### Sequenza di lavoro suggerita
1. Concordare la definizione locale XYZ e fotografare quattro staffe reali, non il solo OBJ.
2. Compilare le schede A4 in officina e trascrivere il CSV.
3. Completare prove di interferenza a ruota libera in più orientamenti, freno inserito/disinserito, manutenzione.
4. Fare convalidare dal carpentiere le quote e produrre un solido CAD del **supporto vero**.
5. Falegname: definire cavità, residuo legno, giunto, ferramenta e setup CNC sulla **staffa vera**.
6. Tecnico: approvare portata, stabilità e ruote; realizzare un prototipo prima della serie.

**Prossimo lavoro vincolante:** ricevere un rilievo completo della carpenteria o un suo modello CAD verificato. Nessuna cavità esecutiva può essere ottenuta dalle box di prova della REV10. Le issue [#6](https://github.com/HGWells2001/time-machine-project/issues/6), [#7](https://github.com/HGWells2001/time-machine-project/issues/7), [#8](https://github.com/HGWells2001/time-machine-project/issues/8) restano aperte.
