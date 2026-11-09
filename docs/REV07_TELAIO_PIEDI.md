# REV07 | Telaio portante nascosto e quattro piedi

**Data:** 9 novembre 2026 · **Stato:** pre-progettazione per carpentiere, falegname, modellista e tecnico strutturale. **NON esecutivo / NON CNC.**

## Elaborati creati e verificati su Google Drive

| Elaborato | Collegamento | Nota |
| --- | --- | --- |
| **Pacchetto REV07 (ZIP)** | [Apri su Drive](https://drive.google.com/file/d/1RPaJcKd7_iMTSe7SbWVm6zwl31C4Aom-/view?usp=drivesdk) | 16 file: dossier, DXF di riscontro, 4 CSV, JSON, scheda carpentiere, fonti, 4 anteprime, manifesto SHA256 e README. Nessun OBJ. |
| **Dossier tecnico A3** | [PDF 12 tavole](https://drive.google.com/file/d/1pzmcDCsO_04I6dw2YKelh6DvWYPBwGb9/view?usp=drivesdk) | Pianta, 4 piedi, catena carichi, sezione concettuale, opzioni architetturali, procedura Coleman, gate. |
| **DXF di studio** | [DXF solo bounding box](https://drive.google.com/file/d/1r1z7ZeNiE2uBdL2i6xoh-qVljw8Pk319/view?usp=drivesdk) | Non forare / non tagliare. Nessun asse ruota, foro o profilo esecutivo. |
| **Coordinate di riferimento** | [CSV](https://drive.google.com/file/d/1-fyult2jymOkcEYjBYSbCBBYkCCyjeRw/view?usp=drivesdk) | P035, P018 e P031-P034, classe G, unità mm e in. |
| **Verifiche strutturali** | [CSV](https://drive.google.com/file/d/1gGZq_27fsop22BVwRfkm-62Jr6pxEwRZ/view?usp=drivesdk) | 10 condizioni, aperte, con responsabilità. |
| **Distinta per preventivi** | [CSV](https://drive.google.com/file/d/1mv0aUKtCZaTu-pWV0OaXWor017Heht8B/view?usp=drivesdk) | Materiali e fasi da specificare; non dimensionati. |
| **Gate di approvazione** | [CSV](https://drive.google.com/file/d/1Tl-q29lLJx1Y419b-_xodwitU85Mkth_/view?usp=drivesdk) | G0-G7, da convalidare prima di produzione. |
| **Dati geometrici REV07** | [JSON](https://drive.google.com/file/d/15DrEoDog1jlsyYONe3qUKsqrPFwrKGNg/view?usp=drivesdk) | Bounding box del modello precedente e provenienza. |
| **Panoramica tavole** | [PNG](https://drive.google.com/file/d/1p2dkfbGA_vNPqmkQG3aupcJ4PNHYwo4I/view?usp=drivesdk) | Contatto visivo di tutte le 12 tavole A3. |

File Drive **privati**; i collegamenti non modificano la condivisione. L'archivio è stato verificato come ZIP integro, senza file OBJ. SHA256 ZIP: `cf1760d2b7b2f302c6c1256b90e5cdc394644ff51f7ad34253aa5a089ca147de`.

## Metodologia Coleman: materiali e sequenza verificati

**Fonte diretta:** [Don Coleman, The Feet (2025)](https://colemanzone.com/Time_Machine_Project/Time%20Machine%20Build%202025/Time%20Machine%20Build%205.htm).

Coleman realizza le parti esterne dei quattro piedi in due mezzi gusci ciascuno: master in schiuma, sagomatura, stuccatura e primer, stampi in silicone, fusione in **resina uretanica pigmentata**. La cavità interna viene ricavata anche mediante prova **vacuform**; gli aggiustaggi richiedono rifinitura manuale. I **supporti metallici per le ruote** sono in acciaio, **tagliato a getto d'acqua e saldato**, su cui si applicano i gusci estetici.

**Fonte di supporto:** [Don Coleman, The Base (2025)](https://colemanzone.com/Time_Machine_Project/Time%20Machine%20Build%202025/Time%20Machine%20Build%201.htm): quattro strati in legno, 2 × 1/2″ e 2 × 3/4″, per **63,50 mm nominali** (non misura della struttura portante).

Questo descrive ciò che Coleman documenta nella sua replica, **non** un elenco di dimensioni di carpenteria originali MGM.

## Coordinate di studio da REV06 e verifica preliminare

`X`: positivo verso console, `Y`: lato, mm. **G = bounding box della geometria OBJ già calibrata ma non certificata.**

| ID | Centro bbox X, mm | Centro bbox Y, mm | Box X × Y, mm |
| --- | ---: | ---: | ---: |
| P031 (anteriore +Y) | +775,92 | +322,39 | 302,35 × 143,90 |
| P032 (posteriore +Y) | −847,98 | +552,76 | 302,35 × 143,90 |
| P033 (posteriore −Y) | −847,98 | −552,75 | 302,35 × 143,90 |
| P034 (anteriore −Y) | +775,92 | −322,39 | 302,35 × 143,90 |
| P035 basamento | centro circa 0 | centro circa 0 | 2233,87 × 1439,48 |

La coppia anteriore risulta **più stretta** di quella posteriore. Questo è un indizio geometrico utile per lo studio del ribaltamento, **ma non autorizza a usare i centri bbox come posizioni delle ruote**. Devono essere rilevati i contatti effettivi caster-pavimento.

## Due architetture lasciate aperte

1. **A. Telaio continuo nascosto**, che riceve i carichi sedia e li trasmette ai quattro supporti.
2. **B. Supporti modulari collegati**, con traverse/piastre da sviluppare, prendendo spunto dalla modularità dei supporti di Coleman.

**Non è stata selezionata alcuna soluzione.** Profilati, bulloni, saldature, piastre, angoli, ruote, portate, baricentro e fissaggi **non sono stati dimensionati**. Le decorazioni in legno e resina **non possono essere presunte portanti**.

### Gate aperti

- [ ] **G0**: scala complessiva e diametro disco convalidati, [issue #1](https://github.com/HGWells2001/time-machine-project/issues/1).
- [ ] **G1**: rilievo dei contatti al suolo e ingombri effettivi ruote.
- [ ] **G2/G3**: massa complessiva, carico occupante, baricentro, stabilità, rating ruote e freni dimensionati da tecnico.
- [ ] **G4**: connessioni della sedia, [issue #5](https://github.com/HGWells2001/time-machine-project/issues/5).
- [ ] **G5**: prova a secco 1:1 con telaio e gusci non portanti.
- [ ] **G6/G7**: esecutivi approvati, produzione controllata e prove documentate.

### Prossima attività

Chiedere un **preventivo separato** per rilievo/progettazione, mock-up, e solo dopo fabbricazione. Vedi [issue #3](https://github.com/HGWells2001/time-machine-project/issues/3) e la scheda sul collegamento sedia/base [REV06](REV06_INTERFACCIA_SEDIA_BASE.md).

**Politica archivio:** nessun OBJ su GitHub; i dati derivati dal vecchio OBJ restano classificati G. I file tecnici sono su Drive privato.
