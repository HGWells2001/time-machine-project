# REV14 | Ricci ornamentali volumetrici di studio (non CNC)

**Data:** 11 novembre 2026 · **Progetto:** replica artigianale 1:1 di _The Time Machine_ (George Pal, MGM 1960) · **Stato:** ipotesi artistica in 3D **NON esecutiva / NON CNC / NON portante**.

## Cosa cambia dalla REV13

Per le **sole due proiezioni laterali** della tavola Perrotta/Coleman (51 tracciati ciascuna) è stata rimossa la piastra rettangolare fittizia della REV13 e ricostruito un **ornamento 3D autonomo, a giorno**, mediante superfici raccordate attorno ai tratti. Due varianti di profondità per lato producono **quattro STL solidi**. Non si è scalato il vecchio OBJ.

**Le quattro proiezioni frontali Perrotta sono rimaste separate e non sono state convertite in quattro falsi piedi 3D.** Questo lavoro non identifica ancora l'esatta corrispondenza fisica delle viste e non descrive le vere cavità, le ruote o la carpenteria. Gli STL REV14 sono studi di scultura ornamentale, non i quattro piedi originali.

## Risorse REV14 verificate su Google Drive (privato)

| Risorsa | Contenuto | Collegamento |
| --- | --- | --- |
| **R130 · ZIP completo** | 24 file: 2 DXF sorgente privati, 4 STL, 7 PNG, dossier PDF, CSV di audit/QA, JSON, script, README e manifest. **0 OBJ.** SHA256: `cfc7d184d511350c37532edb4dd445012dcc7bd397a4f43221127276f8fb22fe`. | [Apri ZIP REV14](https://drive.google.com/file/d/1MAVoavHkYnLsMgjW-CHWR7ubl3U70BUG/view?usp=drivesdk) |
| **R131 · PDF A3** | Otto tavole su fonti, comparazione 3D, quote, QA, lavorazioni e gate | [Dossier REV14](https://drive.google.com/file/d/1MQ1Gbbtt02X4dTqAiO7CGenMFB5fRId8/view?usp=drivesdk) |
| **R132 · PNG** | Comparazione visiva delle quattro sculture | [Panoramica](https://drive.google.com/file/d/1iC76uSMELJYASww1o8d-hskaO0YYk6Ub/view?usp=drivesdk) |
| **R133 · CSV** | Audit X/Z: bbox punti di controllo, estremi matematici cubici e DXF | [Rettifica Bézier](https://drive.google.com/file/d/1p5nCZPTajpC-3ZY_sSo_cDo-WYGHwQvs/view?usp=drivesdk) |
| **R134 · CSV** | Topologia, dimensioni, volumi e hash dei 4 STL | [Registro QA](https://drive.google.com/file/d/1fM7menjZIEQKougjGDulK2ww-drIUGtb/view?usp=drivesdk) |
| **R135 · JSON** | Parametri interpretativi della scultura; niente quote originali di profondità | [Parametri](https://drive.google.com/file/d/1YHWXLCXNy8V6kLz6xMTJbYSMQY2yMn_G/view?usp=drivesdk) |
| **R136 · CSV** | Gate R14-G0…G10 per artista, falegname, carpentiere e tecnico | [Gate](https://drive.google.com/file/d/1NI71bsg2DqxHhjObwYoCI-w7MDIXYZ2v/view?usp=drivesdk) |
| **R137 · PY** | Script Python di generazione dalle due proiezioni DXF REV12; riproducibile senza OBJ | [Generatore 3D](https://drive.google.com/file/d/11p-BEqh9duGT5c1p7glJo36v6OivK_j2/view?usp=drivesdk) |
| **R138 · MD** | README con metodo, fonti, istruzioni e divieti produttivi | [LEGGIMI](https://drive.google.com/file/d/1ezrMdHksPakMeL_n_AJk4MDsv1m6AKMw/view?usp=drivesdk) |

### Quattro STL artistici individuali, NON CNC

| Proiezione | Variante | File | Stato geometrico |
| --- | --- | --- | --- |
| Sinistra | **BASSO**, corpo 14 mm + rilievo 3 mm | [R139 · STL SX basso](https://drive.google.com/file/d/1WyWMhV9FmsceNukjZrU8_n5ATwc5r-kx/view?usp=drivesdk) | Chiuso, unico corpo |
| Sinistra | **ALTO**, corpo 27 mm + rilievo 8 mm | [R140 · STL SX alto](https://drive.google.com/file/d/1Ha8yaNor6w1I8cY0qV6PuidDABYai6ji/view?usp=drivesdk) | Chiuso, unico corpo |
| Destra | **BASSO**, corpo 14 mm + rilievo 3 mm | [R141 · STL DX basso](https://drive.google.com/file/d/18zaC7__osLyP09mC0VNU8g0g9s3YSc2A/view?usp=drivesdk) | Chiuso, unico corpo |
| Destra | **ALTO**, corpo 27 mm + rilievo 8 mm | [R142 · STL DX alto](https://drive.google.com/file/d/1ADJrDpjagn8o_LbWSMPDMzHjH8xm30xN/view?usp=drivesdk) | Chiuso, unico corpo |

**I link Drive sono privati e non modificano i permessi.** Le curve sorgente derivate da materiale Perrotta/Coleman protetto sono soltanto nell'archivio privato; **nessun DXF, OBJ, STL, render del blueprint o ZIP è stato caricato direttamente nel repository pubblico**.

## Rettifica metrica risolta: bbox REV12 contro estremi delle vere curve Bézier

La REV12 aveva riportato il rettangolo `d['rect']` di MuPDF, che include i **punti di controllo** delle curve: questi possono sporgere oltre la Bézier effettivamente disegnata. REV13 aveva misurato i vertici delle 32 campionature Bézier in LWPOLYLINE. REV14 ha risolto il confronto **analiticamente** trovando gli zeri delle derivate cubiche delle coordinate X e Z.

| Elemento | Rettangolo PDF, mm | Bézier effettiva, mm | DXF REV12, mm | Differenza bbox–curva, mm |
| --- | ---: | ---: | ---: | ---: |
| Laterale SX, **X** | 246,317 | **242,917** | 242,914 | 3,399 |
| Laterale SX, **Z** | 155,829 | **151,742** | 151,738 | 4,087 |
| Laterale DX, **X** | 249,262 | **243,480** | 243,474 | 5,782 |
| Laterale DX, **Z** | 155,891 | **151,747** | 151,745 | 4,144 |

La differenza massima della Bézier matematica rispetto al DXF campionato è **0,00592 mm**. È un controllo della **coerenza digitale**, non l'accuratezza metrologica della macchina originale; la scala del disegno resta da verificare nella riproduzione reale.

Le nuove quote corrette integrano, e non cancellano, le precedenti Q-013…Q-017 (che rappresentano il bbox del PDF).

## Tecnica documentata e interpretazione esplicita

**D (documentato):** [Don Coleman, *The Feet*](https://colemanzone.com/Time_Machine_Project/Time%20Machine%20Build%202025/Time%20Machine%20Build%205.htm) mostra master in schiuma scolpito su entrambi i lati, metà guscio separate, vano ricavato per i supporti metallici con ruote e repliche in resina. Non fornisce quote di profondità del riccio MGM né un file CNC per il legno.

**G (dal blueprint):** due gruppi laterali di 51 curve in posizione e scala grafica Perrotta. La loro proiezione non dimostra se un tratto sia un'incisione o un rilievo.

**I (ipotesi del progetto):** dilatazione artistica **7,8 mm** attorno ai tratti, raccordo bordo **5 mm**, varianti BASSO (corpo **14 mm**, coste **3 mm**) e ALTO (corpo **27 mm**, coste **8 mm**). La lavorazione crea un riccio traforato con profilo arrotondato, senza piastra retrostante. Tali profondità **non sono quote MGM**.

**V (da verificare):** interpretazione dei dettagli, sottosquadri, corrispondenza con i quattro frontali Perrotta, posizionamento dei veri ricci nella macchina, spessore del guscio, stabilità e ingombri delle staffe, accesso alle ruote e ferramenta.

## Verifica di produzione (solo mesh)

| Modello | Ingombro X × Y × Z, mm | Facce | Componenti |
| --- | --- | ---: | ---: |
| SX basso | 262,16 × 16,51 × 169,87 | 92.000 | 1 |
| SX alto | 262,51 × 35,26 × 170,14 | 139.464 | 1 |
| DX basso | 262,16 × 16,51 × 169,87 | 91.952 | 1 |
| DX alto | 262,51 × 35,26 × 170,14 | 139.164 | 1 |

**4/4 watertight**, volume positivo, uno stesso corpo per modello. L'ingombro esterno delle sculture supera l'ingombro della sola curva per la dilatazione artistica: non usare i circa 262 mm come quota Perrotta. Una topologia valida non autorizza un CAM né garantisce un vero incastro o una forma autentica.

## Aggiornamento REV15: studio delle viste frontali

La [REV15](REV15_FRONTALI_DUE_FAMIGLIE_CNC.md) ha analizzato **le quattro proiezioni FRONTALI** che nella REV14 erano rimaste esplicitamente separate. Ne risultano due famiglie di tracciati (F1/F4 quasi speculari, F2/F3 quasi identiche) e quattro STL di **linework 3D interpretativo**, ciascuno composto da quattro elementi separati. **Non è stato costruito né validato un solido 3D che unisca le viste laterali e frontali**; la corrispondenza resta aperta, come la carpenteria.

## Gate per la fase successiva

- [ ] Fotografare e identificare quali tratti sono **bordi esterni**, **incisioni**, **rilievi**, ombre o superfici continue sul prop o sulla replica di Coleman.
- [ ] Riconciliare esattamente due viste laterali e quattro frontali. Non dedurre quattro gusci 3D da sei proiezioni scollegate.
- [ ] Scegliere la scultura di riferimento, definire lo spessore reale e semigusci adatti al legno/venatura.
- [ ] Acquisire la carpenteria reale con caster e freni dal [rilievo REV11](REV11_RILIEVO_OFFICINA_CNC.md) / [issue #9](https://github.com/HGWells2001/time-machine-project/issues/9).
- [ ] Disegnare accessi e ritenuta meccanica **smontabile** e verificare la parete residua.
- [ ] Verifica sottosquadri, maschere, registro fronte/retro e simulazione CAM da officina.
- [ ] Prototipo fisico e validazione con modellista, falegname e tecnico. Le parti in legno **non portano il carico**.

**Nessun file REV14 è pronto da fresare.** È un confronto artistico migliorato, e una rettifica metrica verificata, ma non la geometria certificata dei quattro piedi MGM.

Riferimenti: [REV12](REV12_VETTORI_PERROTTA_CNC.md) · [REV13](REV13_RILIEVI_2_5D.md) · [Fonti](FONTI.md) · [Registro delle quote](../data/registro_quote.csv).
