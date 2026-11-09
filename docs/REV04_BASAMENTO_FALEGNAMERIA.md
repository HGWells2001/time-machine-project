# REV04 | Basamento - scheda falegnameria e coordinamento carpenteria
**Data:** 2026-11-09 · **Stato:** pre-progettazione, NON esecutivo.

## Consegnati
- [Pacchetto REV04 su Google Drive (ZIP)](https://drive.google.com/file/d/1OqcNQ5CwJVez-BMedzjLq8qGc4ZFZFVx/view?usp=drivesdk): 15 file, tra cui 10 tavole A3, DXF di riscontro, CSV, schede artigiani e anteprime.
- [Dossier tecnico A3 (PDF)](https://drive.google.com/file/d/1yJnLVKqvBJ3xbih43BT39fKS68hejVGY/view?usp=drivesdk): 10 tavole.

## Adozione documentata del metodo Don Coleman
Coleman (costruzione 2025) documenta 4 dime MDF, 2 strati da 1/2\" e 2 da 3/4\" (totale **2 1/2\" = 63,50 mm**), fresatura dei singoli pannelli mediante 4 frese, impilamento, mordente red mahogany e orange shellac. Non pubblica in quella pagina quattro contorni quotati diversi. L'ordine L1-L4 ripreso dalla REV03 **non e verificato sulla pagina 2025**. [Fonte](https://colemanzone.com/Time_Machine_Project/Time%20Machine%20Build%202025/Time%20Machine%20Build%201.htm).

La pagina Coleman sui [piedi](https://colemanzone.com/Time_Machine_Project/Time%20Machine%20Build%202025/Time%20Machine%20Build%205.htm) mostra gusci estetici in resina uretanica pigmentata, ricavati con stampi in silicone, attorno a supporti in acciaio con ruote. Le parti decorative non devono essere trattate come elementi di portata senza verifica.

## Quote di confronto (NON di taglio)
| Elemento | Millimetri | Pollici | Provenienza |
| --- | ---: | ---: | --- |
| Compensato nominale 1/2\" | 12,70 | 0,5000 | D, Coleman |
| Compensato nominale 3/4\" | 19,05 | 0,7500 | D, Coleman |
| Somma quattro strati | 63,50 | 2,5000 | D, Coleman |
| P035 lunghezza sagoma | 2233,87 | 87,9476 | G, vecchio OBJ |
| P035 larghezza sagoma | 1439,48 | 56,6724 | G, vecchio OBJ |
| P035 altezza mesh | 98,21 | 3,8665 | G, vecchio OBJ |

D = metodo Coleman documentato; G = geometria OBJ derivata dalla calibrazione precedente; V = da verificare. La differenza 98,21 vs 63,50 mm non determina automaticamente un ulteriore pannello: puo derivare dal volume delle modanature o dai riferimenti di misura.

## Stato delle nuove lavorazioni
- [x] Pianta ortogonale di riferimento con impronte P031-P034 come **bounding box**, non forature.
- [x] Schede di tracciatura D1-D4 con quote nominali, senza inventare contorni.
- [x] Schema stratigrafico, prove di modanatura, ordine di montaggio, finitura.
- [x] Distinta e richiesta preventivo per fasi F01-A..E.
- [x] Interfaccia legno / acciaio / rivestimenti non portanti.
- [ ] Correggere scala e ingombri generali dell'OBJ tramite rilievo Perrotta/Coleman e convalidare la misura del disco (issue #1).
- [ ] Definire **davvero** i 4 profili D1-D4, i raggi delle frese, le tolleranze e la disponibilita di compensato.
- [ ] Progettare piastre, collegamenti, sedi sedia, ruote, carichi e stabilita (issue #3).
- [ ] Ottenere revisione da falegname e tecnico prima di autorizzare un CNC.

**Nota:** il DXF allegato conserva la sagoma P035 OBJ come riferimento non chiuso, con layer di avviso e nessun foro. NON e un percorso utensile.
