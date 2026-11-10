# REV11A | Quote esterne dei piedi dalla tavola Perrotta/Coleman

**Data:** 10 novembre 2026 · **Rettifica documentale della REV11** (non nuovi esecutivi). **Nessun OBJ, STL o G-code pubblicato.**

## Aggiornamento 10 novembre 2026: REV12 più precisa

La [REV12](REV12_VETTORI_PERROTTA_CNC.md) ha analizzato **direttamente i tracciati vettoriali** della tavola PDF (non gli screenshot) e il righello grafico da 12 pollici: 86,625 punti PDF, circa 3,518615 mm per punto. Le stime REV11A (250 × 135 × 150 mm, ±15 mm) sono pertanto **superate come riferimento CAD**: non descrivono un unico solido, ma mescolavano proiezioni diverse. I dati vettoriali REV12 separano due ricci laterali di circa 246–249 ×156 mm e quattro sostegni frontali di circa 126 ×134 mm. Gli scassi dei supporti metallici e il volume caster rimangono sconosciuti.

## Fonte originale e metodo

Fonte primaria fornita al progetto: **Chris Perrotta, _Revised Time Machine Drawings7-19.PRINT_, © 1999, rivista da Don Coleman © 2010/2015, una tavola**. [Copia privata della tavola completa su Google Drive](https://drive.google.com/file/d/1ScR74LWQir1dddYwrZUCsf1HCA5OkPdF/view?usp=drivesdk). La tavola dichiara una ricostruzione dimensionalmente accurata del prop MGM 1960 e include **vista laterale**, **vista frontale** e una **scala grafica 0–12 INCHES**.

La scala del campione a raster è circa **208 pixel / 12 pollici = 208 pixel / 304,8 mm**, usando lo stesso PDF renderizzato a 2,5 pixel/pt. Campioni visivi dei contorni delle parti esterne: lati 166/174 px; larghezza frontale 90/94 px; altezza 100/101 px. Si ottengono **letture geometriche e non quote numeriche esplicitamente disegnate**.

## Quote preliminari del guscio ornamentale

| Ingombro | mm | in | Classe | Incertezza prudenziale |
| --- | ---: | ---: | --- | --- |
| **X** lunghezza da vista laterale | **250** | 9,84 | **G-Perrotta** | ±15 mm |
| **Y** larghezza da vista frontale | **135** | 5,31 | **G-Perrotta** | ±15 mm |
| **Z** altezza sotto basamento | **150** | 5,91 | **G-Perrotta** | ±15 mm |

I contorni, le linee di spessore e la non univoca definizione degli estremi rendono queste cifre adatte al **confronto e al pre-preventivo**, non a realizzare dime, grezzi, fori, passaggi ruote o percorsi utensile. La fonte non indica queste dimensioni come tre quote numeriche certificate.

Il precedente OBJ P031–P034 dava circa **302,35 × 143,90 × 180,06 mm**. Lo scostamento è circa **+21% X, +7% Y, +20% Z**. Questo mette in dubbio la scala dell'OBJ per questi particolari: **non correggerlo semplicemente con una trasformazione anisotropa**, perché potrebbe divergere anche la forma. Tutti i vecchi STL REV08–REV10 restano riferimenti di studio, non geometria finale.

## Cosa NON contiene il blueprint

- Geometria interna dei **quattro supporti metallici**, spessori e profili.
- Posizione e diametro di fori, bulloni o staffe per fissaggio dei gusci.
- Dimensioni di ruote, caster, sterzata, oscillazione, freni e relativi inviluppi dinamici.
- Spessore residuo del legno, linea di giunzione, sistema smontabile.

Questi campi restano **V = da verificare** nella [REV11](REV11_RILIEVO_OFFICINA_CNC.md). Le **48 quote dei supporti** NON possono essere riempite attingendo a viste esterne ornamentali. Il validatore deve continuare a riportare **BLOCKED: 0/48** in assenza di rilievo vero. Non confondere la sagoma dei quattro piedi con il volume interno dell'acciaio.

## Risorse verificate e conservate su Google Drive privato

| Risorsa | Collegamento |
| --- | --- |
| **Pacchetto completo REV11A, 7 file**, estratti grafici soltanto a uso privato | [ZIP](https://drive.google.com/file/d/1AQTMW7a6b367IpzdqpLX0dSmWrYknvum/view?usp=drivesdk) |
| **Dossier di confronto e quote** con ritagli della fonte | [PDF A3, 2 pagine](https://drive.google.com/file/d/1Bn1ApPF0dtwOwzb7fHHiRyCmYMwcdsZQ/view?usp=drivesdk) |
| **Rilievo dei singoli campioni e metodo scala** | [CSV pixel → mm/in](https://drive.google.com/file/d/1KxX0DkX9v5_UF--D6e-lPhBYUFLS1tWc/view?usp=drivesdk) |
| **Tre quote riassuntive e campi mancanti** | [CSV classificato G/V](https://drive.google.com/file/d/1MKFPEAuyhNU6k_UWKkgRpqA-_YuceesD/view?usp=drivesdk) |

Il blueprint e i suoi ritagli sono di terzi; **non ripubblicati come immagini nel repository pubblico**. Il dossier su Drive non è stato reso pubblico. I CSV sono derivati dai rilievi del disegno e non sostituiscono il suo copyright.

## Regole per i prossimi lavori

1. Per la forma esterna ornamentale dei piedi, **partire da Perrotta** e riconciliare la geometria anziché prendere l'OBJ come 1:1 certificato.
2. Per gli ingombri interni, progettare il vero supporto con il tecnico/carpentiere: sono componenti che la tavola non dettaglia.
3. Solo dopo la definizione delle due geometrie completare CAD e CAM dei semigusci in legno, mantenendoli **non portanti**.

Riferimenti di avanzamento: [issue #1 scala generale](https://github.com/HGWells2001/time-machine-project/issues/1), [#7 gusci CNC](https://github.com/HGWells2001/time-machine-project/issues/7), [#9 rilievo supporti](https://github.com/HGWells2001/time-machine-project/issues/9).
