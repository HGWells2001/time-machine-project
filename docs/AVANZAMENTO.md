# Avanzamento delle lavorazioni

**Aggiornamento REV15: 2026-11-12 | Fase: pre-progettazione.**

Le parole **preparato** e **documentato** non significano **pronto per costruire**.

## Priorità 1: risolvere le quote generali

- [x] Raccolta tavola Perrotta/Coleman.
- [x] Disponibile OBJ con circa 75 gruppi di geometria.
- [x] Pacchetto 1:1 preliminare con doppia unità mm / in.
- [ ] Identificare tutte le quote originali leggibili sulla tavola, registrando posizione e fonte.
- [ ] Verificare diametro disco, lunghezza, larghezza e altezza rispetto alla replica cinematografica desiderata.
- [ ] Ricalibrare l'OBJ solo dopo aver fissato riferimenti coerenti.
- [ ] Approvare una nuova tavola generale di ingombro.

## Priorità 2: basamento + piedi, REV04

- [x] REV04: dossier A3 di 10 tavole, schede D1-D4, sequenza H0-H7, CSV di controllo e DXF NON CNC ([documentazione](REV04_BASAMENTO_FALEGNAMERIA.md)).
- [x] REV04: richiesta preventivo a fasi per falegname e schema interfaccia supporti metallici.
- [x] Scheda della stratigrafia Coleman: 2 × ½″ e 2 × ¾″, totale 2½″ (63,5 mm nominali).
- [x] Profilo di riferimento dal modello OBJ e posizioni approssimate di quattro piedi.
- [x] Distinzione tra rivestimento estetico e supporto in acciaio.
- [ ] Verificare sagome con quote originali / modello di prova a scala ridotta.
- [ ] Definire essenza e tipo di compensato, collanti, orientamento vene, spessori effettivi disponibili in Italia.
- [ ] Rilevare e approvare quattro dime individuali realmente quotate, profili delle frese e dettagli dei giunti; le schede della REV04 non sono sagome operative.
- [ ] Progettare giunzioni e struttura portante metallica indipendente dalle parti ornamentali.
- [ ] Verificare capacità di carico, stabilità al ribaltamento, rotelle, punti di sollevamento, interfaccia alla sedia.
- [ ] Far approvare gli esecutivi a falegname e tecnico strutturale prima del taglio CNC.

## Priorità 3: sedia

- [x] REV05: tavola 4 viste archiviata nel Drive privato, PDF artigiani 8 pagine e registro mm/in di stime grafiche, con [scheda](REV05_SEDIA_BERNINGHAUS.md).
- [x] REV05: distinta per falegname, intagliatore, tappezziere e carpentiere, più DXF di soli ingombri NON CNC.
- [x] Nuovo OBJ TIMEMACHINE(3) verificato identico alla versione già analizzata; non pubblicato.
- [x] Identificata la Berninghaus 1901 come riferimento citato nella documentazione Coleman.
- [ ] Stabilire modello esatto e differenze rispetto al prop cinematografico.
- [ ] Decidere se reperire/restaurare una sedia originale o costruire una riproduzione in legno.
- [ ] Disegnare struttura resistente e fissaggio al basamento.
- [ ] Definire intagli, imbottitura, tappezzeria e finiture.
- [ ] Testare portata e stabilità prima dell'uso.

## Priorità 3-bis: interfaccia sedia / basamento, REV06

- [x] REV06: dossier 10 tavole A3 e DXF con soli box **NON CNC** ([scheda](REV06_INTERFACCIA_SEDIA_BASE.md)).
- [x] Fonte Perrotta originale S16: piedistallo Berninghaus rimosso; impronte per quattro gambe e due fori di ritenuta non quotati.
- [x] Collocazione di studio ricavata dal catalogo precedente: centro cuscino P018 spostato +153,84 mm in X rispetto a P035.
- [x] Registro G0-G7: strutture, fissaggi e portata non ancora approvati.
- [ ] Rilevare attacchi reali sotto la sedia e definire perimetro resistente.
- [ ] Disegnare e verificare con tecnico un telaio interno, piastre, bulloni, ruote e stabilità.
- [ ] Fare mock-up 1:1, controllo interferenze con i corrimano e la console.

## Priorità 3-ter: telaio portante e quattro piedi, REV07

- [x] Documento REV07 con 12 tavole A3, DXF bbox NON CNC, registro quote e schede artigiani: [vedi REV07](REV07_TELAIO_PIEDI.md).
- [x] Metodo Coleman: quattro supporti d'acciaio con ruote, ricavati per waterjet/saldatura; gusci resina non portanti con stampi silicone.
- [x] Verificata la diversa distanza trasversale tra box piedi anteriori e posteriori, senza assumerli come contatti caster.
- [x] Valutati concettualmente telaio continuo o supporti collegati; nessuno selezionato.
- [ ] Misurare i veri punti di contatto al pavimento, massa e baricentro, ruote/freni e carico occupante.
- [ ] Definire piastre, profilati, saldature, fissaggi e loro verifica strutturale da tecnico competente.
- [ ] Confermare scala MGM, creare prototipo e verificare ingombro dei gusci con accesso alle ruote.

## Priorità 3-quater: gusci ornamentali in legno CNC, REV08

- [x] Preparati otto STL individuali **non watertight**, da P031-P034, ciascuno 312 triangoli, suddivisi lungo Y.
- [x] Confermate due famiglie speculari (P031/P034 e P032/P033), con specularità Y dei semigusci.
- [x] Dossier PDF A3 11 pagine, DXF di silhouette **NON CNC**, distinta, verifica simmetrie, registro dimensioni e gate G0-G8.
- [x] Archivio privato Drive e [documentazione GitHub REV08](REV08_PIEDI_LEGNO_CNC.md), senza pubblicare OBJ.
- [ ] Ricostruire dettagli e superfici corrette su foto cinematografiche/quote convalidate: la mesh è troppo grossolana per rilievi definitivi.
- [ ] Rilevare i supporti reali in acciaio e modellare la cavità interna dei due gusci con legno residuo e giunti smontabili.
- [ ] Preparare veri solidi CAD e simulazioni CAM su CNC a 3 assi, inclusi setup e sottosquadri.
- [ ] Produrre una coppia campione e verificarne l'incastro sul supporto portante prima degli altri tre piedi.

## Priorità 3-quinquies: REV09 solidi e cavita' pilota

- [x] 8 prototipi STL **chiusi e un componente ciascuno**, con voxelizzazione a 2,5 mm e due meta per piede.
- [x] Vano dimostrativo aperto sul giunto Y e due sedi cieche di centraggio per ciascuna meta, senza interpretarle come attacchi reali.
- [x] Generatore locale Python, 4 STL di input, parametri JSON, verifica geometrica CSV; [scheda REV09](REV09_SOLIDI_PROTOTIPO_CNC.md).
- [x] Dossier A3 di nove tavole e archivio ZIP con 26 file, senza OBJ.
- [ ] Rilevare geometria reale supporti acciaio e ruote; sostituire vano dimostrativo con scavo effettivo.
- [ ] Progettare ritenuta smontabile a viti/staffe e accessi, perché i due perni NON serrano i gusci.
- [ ] Ripulire la superfice esterna dalla voxelizzazione e aggiungere gli intagli fedeli al prop.
- [ ] Validare CAM fronte/retro, staffaggi e materiale con falegname prima della produzione.

## Priorità 3-sexies: REV10 rilievi acciaio e cavita parametriche

- [x] REV10: modello con input reale **null** che blocca le generazioni fino alle misure del carpentiere, [scheda REV10](REV10_RILIEVO_SUPPORTI_PARAMETRICO.md).
- [x] JSON di input, generatore Python, 48 quote da rilevare e matrice di controlli G0-G8.
- [x] DEMO fittizia separata, con 8 gusci STL watertight e 8 STEP di ingombro, senza OBJ e senza G-code.
- [x] Dossier A3 di 8 tavole, archivio 34 file con SHA256 verificato e link Drive privati.
- [ ] Carpentiere: rilevare i veri 4 supporti con ruote, incluse sterzata, oscillazione e accesso freno.
- [ ] Falegname/CAD: sostituire box con forma reale e modellare giunto e serraggio smontabile.
- [ ] Falegname/CAM: verificare parete residua, sottosquadri e lavorazioni a due prese.
- [ ] Tecnico: approvare i carichi, i giunti portanti e la stabilita della macchina.

## Priorità 3-septies: REV11 kit rilievo fisico/officina

- [x] [Scheda REV11](REV11_RILIEVO_OFFICINA_CNC.md) con PDF 9 tavole A3 e 4 schede A4 P031-P034.
- [x] CSV 48 misure reali necessarie (tutte vuote), matrice 36 scenari dinamici e frenatura, piano 40 attività per i 4 piedi.
- [x] Validatore Python: su input vuoto restituisce BLOCKED (0/48), su dati simulati coerenti solo per test restituisce MEASUREMENTS_CONSISTENT_NOT_APPROVED; non genera CAD/CAM.
- [x] CSV gate G00-G10 tutti APERTI; JSON con tutti i supporti null.
- [x] Archivio ZIP 15 file, 2 PDF e controlli: nessun OBJ, STL, STEP o G-code.
- [ ] Carpentiere: misurare la vera struttura in acciaio e l'inviluppo ruota, compilare e firmare le schede con foto.
- [ ] Falegname: predisporre CAD dettagliato dei semigusci, cavita, giunti e spessori residui usando rilievo reale.
- [ ] Verificare accesso freni, ruote e smontaggio; mock-up a secco e prove professionali.
- [ ] Tecnico: verificare tutti i carichi, stabilità e parti portanti.

## Priorità 3-octies: REV11A lettura diretta della tavola Perrotta

- [x] Fonte Perrotta/Coleman originale analizzata: vista laterale, frontale e righello grafico 0-12 in.
- [x] Stime **G-Perrotta** dei soli gusci esterni: X=250, Y=135, Z=150 mm, incertezza ±15 mm; [dossier e dati](REV11A_QUOTE_PERROTTA.md).
- [x] Identificata discrepanza del vecchio OBJ 302,35 × 143,90 × 180,06 mm (+21%, +7%, +20% circa): non trasformare automaticamente mesh con scala differente per ogni asse.
- [x] Tre misure aggiunte a `data/registro_quote.csv`; report PDF di 2 pagine e due registri CSV privati su Drive.
- [ ] Riconciliare dettagli artistici e profili del piede fra blueprint e geometria prima dei solidi per CNC.
- [ ] Le 48 quote dei supporti metallici/ruote non figurano nel blueprint e rimangono DA MISURARE/PROGETTARE.
- [ ] Approvatore tecnico e artigiano devono definire cavità, viti, accesso freni e stabilità.

## Priorità 3-novies: REV12 vettori originali Perrotta

- [x] **6 gruppi di curve vettoriali** ricavati direttamente da PDF Perrotta (non dall'OBJ): 2 laterali + 4 frontali, [scheda REV12](REV12_VETTORI_PERROTTA_CNC.md).
- [x] Righello originale 0–12 in letto direttamente: 86,625 punti PDF = 304,8 mm. Curve convertite in DXF R2010 con `INSUNITS=4` e SVG.
- [x] Riccio laterale sinistro 246,3 × 155,8 mm, destro 249,3 × 155,9 mm; quattro sostegni frontali 126,4/126,5 × 133,8 mm (quote grafiche G-Perrotta non CNC).
- [x] PDF A3 6 tavole con scala 1:1 nominale e barra 50 mm; ZIP 24 file integro senza OBJ, script di rigenerazione.
- [ ] Associare correttamente le proiezioni laterali e frontali a veri corpi tridimensionali, senza inventare pareti o giunti.
- [ ] Ricostruire superfici dettagliate di ciascun ornamento e i sottosquadri compatibili con la CNC.
- [ ] Acquisire **48 misure reali** di carpenteria e caster, ancora non presenti sul blueprint.
- [ ] CAD 3D, spessore residuo del legno, simulazioni CAM e approvazione della struttura da professionisti.

## Priorità 3-decies: REV13 rilievi di studio dalle curve Perrotta

- [x] Da 2 tracciati laterali e 4 frontali REV12 generati **6 pannelli 2.5D solidi**, con 4 mm di base e 6 mm di rilievo **I / NON ORIGINALI**; [scheda REV13](REV13_RILIEVI_2_5D.md).
- [x] Sei STL DEMO watertight, volume positivo e un componente per mesh; 6 anteprime PNG.
- [x] Dossier PDF A3 a 8 tavole e generatore riproducibile verificato con ZIP REV12 come input.
- [x] Archivio ZIP 17 file testato, nessun OBJ né G-code; Drive privato e documentazione su GitHub.
- [x] Rilevata discrepanza tra ingombri del CSV REV12 (246,317/249,262 mm) e punti DXF diretti (242,914/243,474 mm), differenza 3,403/5,788 mm.
- [ ] Riconciliare origine degli ingombri laterali e i criteri di inclusione dei contorni.
- [ ] Identificare il **vero numero di corpi** e la corrispondenza tra ricci laterali e sostegni frontali in foto originali.
- [ ] Ricostruire superfici 3D e sottosquadri su evidenza fotografica; vietato presentare il pannello come piede.
- [ ] Ottenere geometria vera delle 4 staffe e delle ruote, definire gli spessori dei gusci, giunti e CAM di officina.

## Priorità 3-undecies: REV14 ricci 3D non portanti e audit Bézier

- [x] Da 51 tracciati per lato REV12 realizzati **4 ornamenti a giorno** STL 3D: SX/DX con varianti BASSO/ALTO, **senza piastra rettangolare REV13**; [scheda REV14](REV14_RICCI_ARTISTICI_3D.md).
- [x] Profondità solo **I / studio**: BASSO 14 + 3 mm, ALTO 27 + 8 mm; nessuna quota di scultura originale MGM dedotta dalle foto.
- [x] **4/4 STL watertight** e monocomponente, QA con volumi, SHA256, 7 anteprime effettive render VTK.
- [x] Risolta matematicamente la divergenza REV12/REV13: bbox PDF include Bézier control points; estremi delle vere curve a SX **242,917 × 151,742 mm**, a DX **243,480 × 151,747 mm** (G-Perrotta 2D; non precisione MGM).
- [x] Quattro nuove righe Q018-Q021 nel registro delle quote, distinguendo bbox PDF dalla geometria della curva.
- [x] ZIP privato di **24 file**, PDF A3 8 pagine, due DXF origine, generatori, tabella di audit e gate. Zero OBJ e nessun STL pubblicato nel repository.
- [ ] Verificare dalle foto quali tratti sono rilievi o incisioni e quali sono veramente superfici scolpite sui gusci.
- [ ] Riconciliare **due laterali e quattro frontali**, senza inventare la corrispondenza ai quattro supporti.
- [ ] Definire i veri supporti d'acciaio, caster/freni e cavità; progettare giunto smontabile e spessore residuo in legno.
- [ ] Verificare sottosquadri, CAM, staffaggi e un solo prototipo fisico prima di una serie.

## Priorità 3-duodecies: REV15 atlante multivista e due famiglie di frontali

- [x] Analizzate direttamente le quattro proiezioni frontali DXF REV12: **F1 e F4 speculari entro 0,0067 mm**, **F2 e F3 coincidenti entro 0,0103 mm**, solo precisione di campionamento digitale.
- [x] Registrate **2 geometrie master** dei 4 frontali, senza attribuzione automatica ai piedi fisici P031-P034. [Scheda REV15](REV15_FRONTALI_DUE_FAMIGLIE_CNC.md).
- [x] **4 STL di prova** ricavati da master A e B con specchio/copia, **watertight ma 4 pezzi separati per STL**, e galleria GLB non assemblata.
- [x] **10 tavole A3**, due pagine alla scala nominale 1:1 con barra verifica 50 mm, confronti, quote, schema non portante e gate.
- [x] **Comparatore HTML offline** con sovrapposizione e specchiatura; script di rigenerazione; matrice **8 corrispondenze frontale/laterale ignote**.
- [x] ZIP di **29 file** SHA256 verificato, 17 risorse private Drive, zero OBJ/G-code; repo GitHub solo link e metodo.
- [ ] Associare immagini della macchina MGM e ricostruzione Coleman alle proiezioni 2D per attribuire le forme a veri corpi.
- [ ] Progettare effettivamente supporti in acciaio con ruote (quelli originali non sono quotati nel Perrotta).
- [ ] Ricostruire scultura 3D completa e non solo ribbon, con cavità, giunti smontabili, spessore legno residuo.
- [ ] Eseguire prototipo CAD/CAM e verifica sicurezza/stabilità con falegname e tecnico.

## Priorità 4: grande disco posteriore

- [x] Segnalata differenza tra riferimento Coleman 60″ e OBJ precedente.
- [ ] Convalidare misura sul corretto allestimento/epoca.
- [ ] Definire mozzo, struttura interna, materiale, supporto, massa e eventuale rotazione.
- [ ] Documentare caratteristiche delle decorazioni, senza assumere che siano strutturali.
- [ ] Progettare fissaggio e protezioni.

## Priorità 5: carpenteria e finiture

- [ ] Corrimano curvati: verificare diametro, raggi, attacchi e materiali.
- [ ] Console e quadranti: disegni per tornio/incisione.
- [ ] Carter e pannelli curvi: campioni e dime.
- [ ] Trattamenti superficiali e riproduzione cromatica.
- [ ] Impianti luce/audio/animazione: studio a bassa tensione e sicurezza elettrica.

## Criteri di chiusura per ogni sottoassieme

Una lavorazione può essere segnata **PRONTA PER PREVENTIVO VINCOLANTE / FABBRICAZIONE** solo se disponibili: fonte quote, revisione congelata, viste e sezioni, distinta materiali, tolleranze, fissaggi, massa, rischio e verifica tecnica applicabile. L'approvazione appartiene all'artigiano responsabile e ai tecnici competenti.

## Archivio esterno

La REV15 frontali multivista è su Drive come `TimeMachine_REV15_FRONTALI_MULTIVISTA.zip`. La REV14 ricci artistici è su Drive come `TimeMachine_REV14_RICCI_ARTISTICI.zip`. La REV13 rilievi DEMO è su Drive come `TimeMachine_REV13_RILIEVI_2_5D.zip`. La REV12 vettori Perrotta è su Drive come `TimeMachine_REV12_PERROTTA_VETTORI.zip`. La REV11A Perrotta è su Drive come `TimeMachine_REV11A_QUOTE_PERROTTA.zip`. La REV11 kit officina è su Drive come `TimeMachine_1960_REV11_RILIEVO_OFFICINA_CNC.zip`. La REV10 parametrici/rilievi è su Drive come `TimeMachine_REV10_KIT_RILIEVI_PARAMETRICO.zip`. La REV09 solidi di prova è su Drive come `TimeMachine_1960_REV09_SOLIDI_PROTOTIPO_CNC.zip`. La REV08 piedi in legno CNC è su Drive come `TimeMachine_1960_REV08_PIEDI_LEGNO_CNC.zip`. La REV07 telaio e piedi è su Drive come `TimeMachine_1960_COLEMAN_REV07_TELAIO_PIEDI.zip`. La REV06 interfaccia sedia/base è su Drive come `TimeMachine_1960_COLEMAN_REV06_INTERFACCIA_SEDIA_BASE.zip`. La REV05 sedia è su Drive come `TimeMachine_1960_COLEMAN_REV05_SEDIA_BERNINGHAUS.zip`. La REV03 sul basamento/piedi è disponibile su Google Drive con nome `TimeMachine_1960_COLEMAN_REV03_BASAMENTO_PIEDI.zip`. Questo repository conserva lo stato e i riferimenti, non dichiara automaticamente approvate le tavole dell'archivio.
