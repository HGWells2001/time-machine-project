# REV13 | Sei pannelli di rilievo 2.5D da curve Perrotta

**Data:** 11 novembre 2026. **Oggetto:** continuità della replica artigianale 1:1 della macchina del tempo di George Pal (1960). **Stato:** modelli tridimensionali di visualizzazione/pre-progettazione, **NON CNC** e **NON fedeli a una profondità originale documentata**.

## Risultato effettivo

Sono stati realizzati **6 pannelli solidi 2.5D** a partire dalle **6 proiezioni REV12**:
- due ricci ornamentali laterali;
- quattro profili in vista frontale.

I tracciati estratti da Perrotta sono **curve aperte**; perciò **non è giustificato chiuderli automaticamente o fonderli in quattro piedi tridimensionali**. La REV13 visualizza soltanto l'andamento in rilievo di quelle linee. Non sono progettati piedi fisici, facce posteriori, cavità interne, bulloni o supporti ruota. I supporti d'acciaio restano indipendenti e non dimensionati.

## Materiali verificati su Google Drive privato

| Tipo | Risorsa | Collegamento |
| --- | --- | --- |
| **ZIP, 17 file** | Pacchetto completo REV13, sei STL, sei PNG, PDF A3, CSV, JSON, script e README; 5,79 MB, 0 OBJ | [Apri su Drive](https://drive.google.com/file/d/1AeUp6kI7Sw8nkvT_icxESQQcWzG5pbM7/view?usp=drivesdk) |
| **PDF** | Dossier tecnico di **8 pagine A3**, metodo, viste, QA, limiti e istruzioni per il modellista | [Dossier A3](https://drive.google.com/file/d/1OEYP_NR15HSttJlX_3GwldgAKP_lUjz5/view?usp=drivesdk) |
| **CSV** | Controllo dei sei STL: ingombri, SHA256, linee sorgente, volume e validazione topologica | [Verifiche mesh](https://drive.google.com/file/d/1bA2ca6q0J4Xewx5t8T_2XgBm53Upjplp/view?usp=drivesdk) |
| **JSON** | Parametri di studio, con provenienza distinta G/I | [Parametri interpretativi](https://drive.google.com/file/d/1h05qp2PUREtTp-Tml8pJVO2nz6_XjOk-/view?usp=drivesdk) |
| **Python** | Generatore che legge il **ZIP REV12 privato** e ricostruisce i 6 pannelli; riproduzione testata | [Generatore REV13](https://drive.google.com/file/d/1RQAlobC3aQjiUe_zf00UgwKO2_OSqcH2/view?usp=drivesdk) |

### Sei STL di studio individuali

| Proiezione | Tratti aperti | File |
| --- | ---: | --- |
| Laterale sinistro | 51 | [STL sinistro](https://drive.google.com/file/d/1m3yNzw_nr-x4yAYpo5qRLNd4tAPgbQPE/view?usp=drivesdk) |
| Laterale destro | 51 | [STL destro](https://drive.google.com/file/d/1eIU-Fs-0qVe4ZALW5lMjZqYig2afdcnj/view?usp=drivesdk) |
| Frontale F1 | 10 | [STL F1](https://drive.google.com/file/d/177sR2E7Uprs3iUvi03TQjSaE8A_JHg3g/view?usp=drivesdk) |
| Frontale F2 | 12 | [STL F2](https://drive.google.com/file/d/1UCSQXn_QQ1r_HZ7_i4WVh9EczAWOdIAx/view?usp=drivesdk) |
| Frontale F3 | 12 | [STL F3](https://drive.google.com/file/d/1oUbxEOunY__aIe3LEeqXsVk6Awwc7Grz/view?usp=drivesdk) |
| Frontale F4 | 10 | [STL F4](https://drive.google.com/file/d/1VHslrXC7RtqzsWXr14y9dTpvkgucIiHW/view?usp=drivesdk) |

**Nessuno STL è pubblicato su GitHub**, perché la superficie è derivata dalle curve del blueprint protetto. I file Drive restano privati.

## Distinzione dei dati

**G - dal blueprint Perrotta (REV12)**: andamento delle curve 2D e loro collocazione nelle viste laterali e frontali; provenienza [S01](FONTI.md).

**I - ipotesi introdotte in REV13**: un pannello piano rettangolare con **4 mm** di base; linee tradotte in rilievi positivi con altezza **0–6 mm**, margine **10 mm**, passo della griglia **1,5 mm** e smoothing gaussiano. **Queste profondità NON sono misurate sul prop**. Non dedurre da questa impostazione uno spessore di guscio, una geometria 3D MGM, né un metodo CNC approvato.

**V - ancora da verificare**: corrispondenza fisica tra viste, profondità reale di ogni riccio, sottosquadri, facce posteriori, linea giunzione gusci, acciaio interno, caste(r)/ruote, freni, portata, giunti. Vedi [REV11 rilievo officina](REV11_RILIEVO_OFFICINA_CNC.md) e [issue #9](https://github.com/HGWells2001/time-machine-project/issues/9).

### Aggiornamento REV14

La [REV14](REV14_RICCI_ARTISTICI_3D.md) ha risolto la discrepanza dei bounding box: le estensioni della REV12 derivano dal **rettangolo dei punti di controllo Bézier**, quelle della REV13 dalla **polilinea campionata**. Gli estremi matematici coincidono col DXF entro 0,006 mm. I quattro STL della REV14 sono inoltre **ornamenti autonomi a giorno**, non pannelli rettangolari; restano interpretazioni, non i piedi originali.

## Discrepanza di misura rilevata nei DXF

Il **CSV quote REV12** riportava le larghezze laterali **246,317 mm (SX)** e **249,262 mm (DX)**. Il ricalcolo degli estremi dei **vertici LWPOLYLINE dei DXF REV12**, usati dal generatore, restituisce invece **242,914 mm (SX)** e **243,474 mm (DX)**. Gli scostamenti sono rispettivamente **3,403 mm** e **5,788 mm**. Questi due metodi di bounding box **sono stati riconciliati nella REV14**. Non sostituire automaticamente le quote G ufficiali; registrare il conflitto e verificare possibili tratti/campionamento/coordinate prima di qualunque elaborato definitivo.

Per i quattro frontali le misure da vertici DXF sono circa **126,44–126,45 × 133,82 mm**, coerenti con REV12.

## Controlli effettuati

- [x] Analisi dei sei DXF REV12: **nessuna polilinea sorgente chiusa**, perciò non è stato ricostruito un finto contorno del piede.
- [x] Generati sei **pannelli triangolati con top e bottom chiusi**, ciascuno un unico solido.
- [x] Controllo `trimesh`: **6/6 watertight**, volume positivo, un componente collegato.
- [x] Realizzati sei PNG con mappa delle altezze e ombreggiatura di studio.
- [x] PDF di 8 pagine A3 renderizzato e rivisto.
- [x] Generatore REV13 eseguito una seconda volta con ZIP REV12 come input: **sei modelli rigenerati con successo**.
- [x] Archivio REV13 verificato con test ZIP, **17 membri**, **0 OBJ** e **0 G-code**. SHA256 ZIP `801e7327d68daef951d893f6a0b4bc9f4f473cb342ff33986bd86fdf6d8373f4`.

Un pannello **watertight** è solo una verifica di topologia. Non conferma la corrispondenza all'originale, la lavorabilità, la qualità del rilievo o la portata.

## Gate per REV14, verso un modello ornamentale autentico

1. Chiarire la corrispondenza tra **2 proiezioni laterali** e **4 frontali**, usando fotografie del prop e non solo curve isolate.
2. Decidere quali linee siano bordi esterni, intagli, ombreggiature e superfici in rilievo. **La REV13 le tratta tutte come tracce positive** solo per studio.
3. Ricostruire superfici artistiche in CAD/scultura digitale con profondità e retro proposti e poi verificati visivamente.
4. Prima di realizzare i **semigusci in legno CNC**, avere il supporto vero in acciaio, gli ingombri ruote e il fissaggio smontabile.
5. Eseguire campione fisico, controllo sottosquadri e simulazione CAM dell'officina, poi approvazione del tecnico per le parti portanti.

**Non usare come file di fresatura, stampo o componente portante.** La REV13 è una revisione di *visualizzazione volumetrica del tratto*, non una certificazione del piede originale MGM.

Progetto principale: [README](../README.md) · [REV12 vettori](REV12_VETTORI_PERROTTA_CNC.md) · [fonti](FONTI.md) · [revisioni](REVISIONI.md).
