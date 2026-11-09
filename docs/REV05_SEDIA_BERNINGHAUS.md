# REV05 | Sedia Berninghaus 1901 per la Time Machine 1960

**Data:** 9 novembre 2026. **Stato:** dossier di pre-progettazione per falegname, intagliatore, tappezziere e carpentiere. **Non è una tavola esecutiva né un file di taglio CNC.**

## File verificati su Google Drive (privato)

| Risorsa | Link | Contenuto |
| --- | --- | --- |
| **REV05 completo (ZIP)** | [Apri su Drive](https://drive.google.com/file/d/1FQbZ7MlEyPljM4TcKHJ-YK1-ugOIyuhp/view?usp=drivesdk) | 12 file: dossier A3, misure CSV/JSON, DXF di solo ingombro, richieste artigiani, checklist, estratti privati di confronto |
| **Dossier sedia (PDF A3)** | [Apri su Drive](https://drive.google.com/file/d/1DqilJCFYDdBwHyBP_pYTBJg7ltDD14SW/view?usp=drivesdk) | 8 tavole di lavoro |
| **Tavola originale «Time Saddle»** | [Copia privata su Drive](https://drive.google.com/file/d/16c75RXaJoStxhi0dZESMZRg4osjyzDHn/view?usp=drivesdk) | Le 4 viste, scala grafica in pollici; © Don Coleman 2010, rev. 2015. Non ripubblicare su GitHub |
| **Registro misure** | [CSV](https://drive.google.com/file/d/1Kr8LVjkro6RFwYtYzcyj_RXAaGwxQyLm/view?usp=drivesdk) | Stime in mm e pollici con fonte |
| **DXF ingombri** | [DXF NON CNC](https://drive.google.com/file/d/1W3_ru-66yogmDwQQbsRHhtF_zflk5jca/view?usp=drivesdk) | Tre rettangoli di confronto, **NON** contorni delle parti |
| **Distinta preliminare** | [CSV](https://drive.google.com/file/d/1E1taJ-hSOgyWm86Ha9r3x0qwbxn5sj9a/view?usp=drivesdk) | Dodici voci divise per artigiano |

I file Drive restano privati. Nessun OBJ è stato pubblicato né inserito nello ZIP REV05.

## Misure grafiche ricavate dalla tavola originale

La tavola presenta **pianta, laterale, frontale e posteriore** e barra da **0 a 12 pollici**, usata per un rapporto di scala. Il profilo risultante NON costituisce una quota di fabbricazione certificata.

| Vista | Dimensioni indicative | Unità |
| --- | --- | --- |
| Pianta | larghezza ~667; profondità ~757 | mm |
| Laterale | profondità ~748; altezza ~903 | mm |
| Frontale | larghezza ~660; altezza ~906 | mm |
| Posteriore | larghezza ~650; altezza ~899 | mm |
| **Ingombro di confronto arrotondato** | **670 × 750 × 900** | **mm (L × P × H)** |

Classificazione **G = lettura geometrica** e **±25 mm prudenziali**, per sola pianificazione. Quote vere di montanti, fori, materiale, elevazione seduta, portata e interfacce **da rilevare**. La scala stampata del PDF deve essere verificata su un test di stampa.

## Metodo di Don Coleman recepito, con provenienza

Fonte: [Don Coleman, The Chair (Build 2025 / Part 2)](https://colemanzone.com/Time_Machine_Project/Time%20Machine%20Build%202025/Time%20Machine%20Build%202.htm).

- La sedia usata nel film è descritta da Coleman come una **Berninghaus da barbiere, modello 1901**. Il testo racconta una sequenza di repliche con sedia costruita personalmente e uso/restauro successivo di un esemplare d'epoca; **non mescolare le varianti**.
- Il **poggiapiedi originale** fu usato come **poggiatesta** nella versione cinematografica.
- Coleman descrive una nuova costruzione del poggiatesta, decorazioni laterali, rosette, imbottitura e fregi laterali rifatti quando alcuni erano andati perduti.
- La possibile presenza di **altoparlante nel poggiatesta** appartiene alla replica per un cliente e **non è un dettaglio cinematografico documentato come originale**.
- Materiali e struttura portante proposti nella REV05, inclusi legno massello e rinforzi, sono **ipotesi da discutere con falegname e tecnico**, non misure strutturali pubblicate da Coleman.

## Parti per mestiere

| Artigiano | Elementi |
| --- | --- |
| Falegname | Telaio seduta, schienale, montanti, braccioli e poggiatesta |
| Intagliatore / modellista | Rosette, bassorilievi floreali, motivi laterali, fregio inferiore |
| Tappezziere | Seduta, schienale trapuntato, braccioli e poggiatesta |
| Carpentiere | Giunti al basamento e parti eventualmente portanti in metallo |
| Tecnico qualificato | Verifica portata, stabilità e uso da parte di persone |

**Non autorizzare taglio CNC né fissaggi portanti con le quote grafiche di REV05.** La sedia e il basamento devono essere progettati e verificati insieme.

## Nuovo file OBJ ricevuto

Il file `TIMEMACHINE(3).obj` è stato controllato **localmente**: SHA256 identico al precedente `TIMEMACHINE(2).obj`: `98354729da576e7f7760b6940b32e6310e939cd4dba2ee25c65b16fa4661edcb`. Non introduce una nuova geometria da ricalibrare e **non è stato caricato su GitHub né allegato al dossier REV05**.

## Gate per REV06

- [ ] Approvazione delle dimensioni generali della replica: [issue #1](https://github.com/HGWells2001/time-machine-project/issues/1).
- [ ] Dati reali seduta / montanti / traverse / braccioli / fregi / poggiatesta.
- [ ] Scelta definitiva fra replica in legno e restauro Berninghaus (preferenza iniziale: replica in legno).
- [ ] Integrazione meccanica con REV04 del basamento: [issue #2](https://github.com/HGWells2001/time-machine-project/issues/2).
- [ ] Controllo struttura metallica di base: [issue #3](https://github.com/HGWells2001/time-machine-project/issues/3).
- [ ] Mock-up, campioni, cartamodello, prova portata e revisione degli artigiani.
