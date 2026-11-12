# REV15 | Frontali Perrotta: due famiglie, quattro modelli di studio e atlante multivista

**Data:** 12 novembre 2026 · **Stato:** rilievo geometrico/interpretazione artistica **NON CNC, NON esecutiva, NON portante**.

Questa revisione prosegue [REV14](REV14_RICCI_ARTISTICI_3D.md). A differenza dei due ricci ornamentali laterali di REV14, qui si analizzano le **quattro proiezioni frontali** della tavola Perrotta/Coleman, preservando l'incertezza sulla loro corrispondenza ai componenti fisici. **Non esiste ancora un vero piede 3D ricostruito dall'incrocio delle proiezioni.**

## Risultato accertato: quattro frontali, due famiglie di tracciati

I profili sono curve **aperte** nel piano locale U–Z e misurano circa **126,45 × 133,82 mm** (geometria G derivata dal blueprint; non quota certificata MGM).

L'analisi bidirezionale con ricerca del punto più vicino sui vertici campionati dei DXF fornisce:

| Coppia | Confronto geometricamente più vicino | Scostamento massimo |
| --- | --- | ---: |
| **FRONTE_1 / FRONTE_4** | F4 specchiato sull'asse locale U=63,225 mm | **0,0067 mm** |
| **FRONTE_2 / FRONTE_3** | Senza specchiatura | **0,0103 mm** |
| Tra una proiezione della famiglia F1/F4 e una F2/F3 | Distinte | circa **33,85 mm** |

Le differenze sono **coerenza digitale delle proiezioni campionate**, non tolleranze di fabbricazione. Ne consegue un possibile risparmio di lavoro CAD: **master A = F1 con F4 derivato per specchio; master B = F2 con F3 derivato per copia**. Sono famiglie di *tracciati frontali*, non prove che gli otto semigusci dei quattro piedi siano riducibili a soli due componenti.

**Verifica del vincolo 3D:** la vista laterale contiene due ricci, la frontale quattro proiezioni. Sono state censite **otto possibili associazioni**, tutte segnate **NON DETERMINATA**; non è autorizzato assegnarle ai piedini P031-P034.

## Materiale REV15 verificato su Google Drive privato

| Risorsa | Contenuto | Link |
| --- | --- | --- |
| **R143 · ZIP** | **29 file, 6,98 MB**, include 6 DXF sorgenti privati, 4 STL, 1 GLB, PDF 10 tavole, registri, generatore, comparatore HTML e anteprime; SHA256 `c853fecd80fed43c53645205342b070e45f644a7d4f49ecb0eb474af7e4bf34a`; **0 OBJ e G-code** | [Pacchetto REV15](https://drive.google.com/file/d/1jjEdiSwOu3pzYq_YHkrOTkTBJHnUXohT/view?usp=drivesdk) |
| **R144 · PDF A3** | **10 tavole**, incluse due pagine con coppie F1/F4 e F2/F3 a **scala nominale 1:1** e segmento di controllo stampa 50 mm | [Dossier](https://drive.google.com/file/d/1KKdvhp9mGhY7m5gh8SAD-NjPdRJaIU5B/view?usp=drivesdk) |
| **R145 · PNG** | Quattro render frontali effettivi | [Anteprima](https://drive.google.com/file/d/1jf8RZ-W5i8mPHlXaO9Oh4D5pR8XZ95BH/view?usp=drivesdk) |
| R146 · CSV | Scostamenti diretti/specchiati per tutte le sei coppie | [Simmetrie](https://drive.google.com/file/d/17hE6P1gIMhHQqnwxOLaxUlAZ8oiF9Tre/view?usp=drivesdk) |
| R147 · CSV | Inventario delle sei proiezioni, dimensioni e tracciati aperti | [Inventario](https://drive.google.com/file/d/1XFxsvsTKZn1ChLHMRFtO-YU-Bhi8bxa_/view?usp=drivesdk) |
| R148 · CSV | Otto combinazioni frontale/laterale **non ancora attribuibili** | [Matrice associazioni](https://drive.google.com/file/d/18Z_z6USVmcDqcc8T8vlqyKZ4Y46fMulN/view?usp=drivesdk) |
| R149 · CSV | QA dei quattro STL, componenti, dimensioni, topologia e SHA256 | [QA mesh](https://drive.google.com/file/d/1z6L7Ca8bdhYxgg6HJu1dD_X6a4czX2kB/view?usp=drivesdk) |
| R150 · JSON | Parametri della **ricostruzione interpretativa**, categoria I | [Parametri](https://drive.google.com/file/d/1GBB4vLSSMzQG9EOzPINAprCsLUxuyOIm/view?usp=drivesdk) |
| R151 · CSV | Dieci controlli G0–G9, nove ancora aperti; G1 limitato a coerenza digitale | [Gate](https://drive.google.com/file/d/1-IrFNLYTH_-P8-TLk_m6n6d2Tc3G4rH8/view?usp=drivesdk) |
| **R152 · HTML** | Comparatore **totalmente offline**, con scelta di profili, specchiatura e overlay su reticolo in mm | [Apri/scarica comparatore](https://drive.google.com/file/d/1U3eDs7Xbag74IsDdWX37Su_OoDcP5P_s/view?usp=drivesdk) |
| R153 · Python | Generatore per riprodurre gli STL e il dossier dai sei DXF privati | [Script rigenerazione](https://drive.google.com/file/d/157kfIqh2eXF_zuFtOA4oMfa5-OwWpMg8/view?usp=drivesdk) |
| **R154 · GLB** | Galleria di quattro frontali *distanti tra loro*, **NON assieme della macchina** | [Galleria 3D](https://drive.google.com/file/d/13Geez_dmdBCD0buaB5z7tVz8nmUMDRuW/view?usp=drivesdk) |
| R155–R158 · STL | Quattro interpretazioni volumetriche delle **tracce frontali**, separate in quattro componenti ciascuna | [F1](https://drive.google.com/file/d/1Of5ZBK8y-PuaIKSmu0EJOsQQHYgYTzdu/view?usp=drivesdk) · [F2](https://drive.google.com/file/d/13ZECDktQ2i-qt29yGIFnZyCRBhrUT3fr/view?usp=drivesdk) · [F3](https://drive.google.com/file/d/1-EiD9CEf6tJ-DcBIoa6O4rbywmjGKdBm/view?usp=drivesdk) · [F4](https://drive.google.com/file/d/1Ld1yBo32O6MZfKJN0Dk9sTHIhcv5cdBD/view?usp=drivesdk) |
| R159 · PNG | Atlante delle sei proiezioni distinte | [Atlante](https://drive.google.com/file/d/1jmqaypD0xuyoTdFci-bACG7yUGbrVu-y/view?usp=drivesdk) |

**Privacy e copyright:** i disegni DXF e l'HTML che incorpora le curve sono **solo nell'archivio Google Drive privato**, non nel repo pubblico. Non sono stati pubblicati OBJ/STL/GLB, DXF o ZIP su GitHub. I link sono privati e non cambiano i permessi.

## Cosa significano i quattro STL

I quattro modelli sono **strisce ornamentali di studio**, ottenute ispessendo tratti aperti originali su un piano ortografico:
- **G**: posizione delle curve frontali Perrotta (approssimate con polilinee REV12).
- **I**: raggio fittizio del tratto **4,0 mm**, corpo profondo **10,0 mm**, cresta aggiuntiva **2,0 mm**, voxel **0,9 mm**.
- **V**: oggetto fisico corrispondente, spessore reale, eventuali sottosquadri, superfici continue, lato posteriore, giunti, ruote/supporti.

Tutti i **4/4 STL sono watertight**, ma **ognuno contiene quattro corpi scollegati**. L'intero ingombro della rappresentazione ipotetica è circa **137 × 12 × 144 mm**, non coincide con il bounding box della sorgente **126 × 134 mm** perché il tratto è stato ispessito. Non sono quindi gusci reali né file CNC; la galleria GLB non è un assemblaggio.

## Verifiche e limiti

- [x] 4 DXF frontali e 2 DXF laterali d'origine verificati in **millimetri**.
- [x] Classificazione in **due famiglie** e matrice completa di 6 coppie (Hausdorff sul campionamento, non precisione MGM).
- [x] Quattro STL chiusi, **quattro componenti indipendenti ciascuno**, 1 GLB galleria con modelli separati.
- [x] 10 pagine PDF A3 verificate mediante rendering e testo; due tavole con barra da 50 mm: **stampare al 100%**.
- [x] Comparatore standalone senza API, cloud, server o installazioni.
- [x] ZIP verificato integro, **29 file**, SHA256 presente, **zero OBJ/G-code**.
- [ ] Fotografie di riferimento da più direzioni per attribuire le proiezioni a pezzi reali.
- [ ] Modello artistico 3D autentico e continuo, con quote/tolleranze approvate.
- [ ] Misura/progetto dei **quattro supporti in acciaio** con ruote, sterzata e freni (REV11).
- [ ] Gusci in legno con cavità, spessore residuo, piano di separazione, ritenuta smontabile.
- [ ] Campione fisico, simulazione CAM, approvazione di falegname/carpentiere e verifica portante.

**Conclusione:** REV15 è una riduzione della complessità delle *viste frontali* e un kit di confronto per il modellista, non un progetto esecutivo dei quattro piedi.

Fonti: [Perrotta / Coleman S01](FONTI.md) · [Coleman, The Feet 2025](https://colemanzone.com/Time_Machine_Project/Time%20Machine%20Build%202025/Time%20Machine%20Build%205.htm). Coleman documenta gusci in due metà di resina che racchiudono acciaio e ruote; **il legno CNC è una variante proposta**.

Revisioni correlate: [REV12](REV12_VETTORI_PERROTTA_CNC.md), [REV13](REV13_RILIEVI_2_5D.md), [REV14](REV14_RICCI_ARTISTICI_3D.md), [REV11](REV11_RILIEVO_OFFICINA_CNC.md).
