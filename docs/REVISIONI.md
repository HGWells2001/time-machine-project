# Registro revisioni

| Data | Revisione | Oggetto | Esito | Limite |
| --- | --- | --- | --- | --- |
| 2026-11-08/09 | Base OBJ 1:1 preliminare | Calibrazione, separazione di 75 geometrie | Materiale di studio | Scala da confermare sulle fonti originali |
| 2026-11-09 | Doppia quotatura | Dime PDF e DXF metrici con riferimento in pollici | Materiale per confronto artigianale | Nessun file esecutivo certificato |
| 2026-11-09 | REV02 Coleman | Ricerca metodi di lavorazione, studio disco, distinta per artigiani | Dossier metodologico | Le tecniche vanno adattate/verificate |
| 2026-11-09 | REV03 basamento/piedi | Pianta ortogonale, stratigrafia nominale, posizioni preliminari, schema supporti | Pre-progettazione | Quote/attacchi/portate da validare |
| 2026-11-09 | REV04 falegnameria | Dossier A3 (10 pagine), DXF di riscontro P035, D1-D4 da rilevare, campioni, gates H0-H7, distinta e preventivo | Pacchetto e dossier su Drive, tracciamento su GitHub | Non sono state prodotte dime esecutive o forature approvate |
| 2026-11-09 | GitHub tracking 0.1 | README, avanzamento, quote, issue aperte | Registro iniziale | Non modifica gli elaborati CAD esistenti |

| 2026-11-09 | GitHub indice fonti e risorse | Pubblicati `docs/FONTI.md`, `docs/ARCHIVIO_RISORSE.md` e `data/catalogo_risorse.csv` con 17 link Drive e fonti esterne | Cataloghi su branch main; aggiunto `.gitignore` per OBJ e ZIP | Link Drive privati; nessun OBJ pubblicato su GitHub |

| 2026-11-09 | REV05 sedia Berninghaus | Quattro viste originali, stime grafiche 670 × 750 × 900 mm, dossier 8 pagine, DXF ingombri NON CNC e distinta mestieri | ZIP e PDF su Drive; scheda e fonti su GitHub | Quote da rilievo, portata e giunti da validare; nessun OBJ pubblicato |

| 2026-11-09 | REV06 interfaccia sedia/base | Dossier 10 tavole, sovrapposizione bbox P035/P018, catena quote Z, percorso carichi, checklist, DXF NON CNC | 8 risorse su Drive e registri su GitHub | Progettazione strutturale / scala generale / fori reali ancora BLOCCATI; nessun OBJ pubblicato |

| 2026-11-09 | REV07 carpenteria nascosta e piedi | Dossier 12 tavole, DXF bbox NON CNC, 4 CSV, JSON, fonti Coleman e controllo dei carichi | 9 risorse Drive, schema su GitHub, 16 file nel pacchetto | Tutti i carichi, appoggi e fissaggi restano da dimensionare da tecnico; nessun OBJ pubblicato |

| 2026-11-09 | REV08 piedi ornamentali in legno CNC | 8 STL superfici aperte, 11 tavole A3, DXF silhouette, 4 registri, JSON, schede artigiani e anteprime | 18 nuove risorse Drive, scheda e fonti GitHub | Non contiene cavità, solidi chiusi, giunti o G-code; nessun OBJ pubblicato |

| 2026-11-09 | REV09 solidi demo piedi CNC | Ricostruzione voxel 2,5 mm, 8 STL solidi watertight, tasca pilota, sedi perni, script rigenerabile, PDF A3 9 pagine | 16 risorse nuove Drive e registrazione su GitHub | Cavità e fori di centraggio dimostrativi, serraggio non progettato, G-code assente, nessun OBJ pubblicato |

| 2026-11-10 | REV10 rilievo e modello parametrico | Kit 34 file, generatore con stop sui valori null, 8 gusci STL DEMO e 8 STEP inviluppi fittizi, 8 tavole A3 e schede quote | 12 risorse Drive collegate, registrazione GitHub, SHA256 ZIP verificato | Supporti reali NON misurati; scassi DEMO NON CNC; nessun OBJ o G-code pubblicato |

| 2026-11-10 | REV11 kit rilievo officina e validatore | 9 tavole A3, 4 schede A4, 48 quote/36 scenari/40 attività, script di validazione senza geometria | ZIP e 9 risorse individuali su Drive, 10 link su GitHub | Misure reali assenti (BLOCKED); carichi e giunti non approvati; zero OBJ pubblicati |

| 2026-11-10 | REV11A estrazione quote Perrotta | Misurati dal righello 0-12 in e viste ortogonali ingombri esterni ornamentali 250 × 135 × 150 mm ±15; report A3, due CSV, 7 file ZIP | Quattro risorse Drive private e documento GitHub | Non sono quote numeriche della tavola; staffe, fori e ruote NON documentati, 48 campi REV11 ancora vuoti |

| 2026-11-10 | REV12 curva Perrotta vettoriale | Estratte 6 proiezioni dal PDF vettoriale, 6 DXF mm/6 SVG, PDF A3 6 tavole, script e QA; scala da righello 12 in | ZIP 24 file, 11 nuove risorse Drive, relazione GitHub, registro quote aggiornato | Le linee non sono contorni CNC, le proiezioni non formano 3D certo, staffe/ruote non quotate; nessun OBJ |

| 2026-11-11 | REV13 rilievi 2.5D Perrotta | Generati 6 pannelli STL chiusi da curve REV12, 6 PNG, 8 tavole A3, CSV QA e script con prova di rigenerazione | ZIP 17 file su Drive privato; 18 risorse indicizzate, 129 totali; scheda GitHub | Profondità DEMO 6 mm e piastra 4 mm INVENTATE; 6 pannelli non sono 4 piedi 3D; divergenza DXF/CSV REV12 aperta; 0 OBJ pubblicati |

## Regole di revisione

- Ogni nuova revisione deve elencare: cosa cambia, perché, fonti, parti coinvolte, controlli superati e domande aperte.
- Conservare sempre i riferimenti ai pacchetti originali; non sostituire un file tecnico senza un numero di revisione.
- Distinguere **approvazione geometrica**, **approvazione per preventivo** e **approvazione per costruzione**.
- Le tavole originali Perrotta/Coleman sono materiale di riferimento. Non ripubblicare copie integrali senza autorizzazione.
