# L'Invisibile in Rete
Sito divulgativo statico per il **Modulo 5 — Linee, Antenne e Telecomunicazioni** del corso di Elettronica per la classe 5ª ITIS (17–19 anni). Il contenuto deriva dalla presentazione *Linee, Antenne e Telecomunicazioni.pptx* e ne riorganizza i 37 slide in un percorso navigabile.
Nessuna dipendenza, nessun passaggio di build: HTML, CSS e un po' di JavaScript vanilla.
## Contenuti
| Sezione | Argomenti principali |
|---|---|
| **Mappa del corso** | Roadmap del programma biennale TLC (80 ore) |
| **1 · Fisica ed elettromagnetismo** | Campi E e B, sintesi di Maxwell, onda trasversale, polarizzazione, λ = c/f, trigonometria dell'onda (f, ω, φ) |
| **2 · Linee di trasmissione** | Coassiale, bifilare, microstriscia; impedenza caratteristica Z₀; onda diretta e riflessa, Γ, ROS; adattamento e trasformatore λ/4; condizioni di non distorsione |
| **3 · Antenne** | Dipolo hertziano e a mezz'onda, antenna Marconiana, pannelli, Yagi, paraboliche; polarizzazione; antenna isotropica (0 dBi); diagramma di irradiazione, −3 dB, rapporto A/I; efficienza, guadagno, EIRP |
| **4 · Modulazioni AM e FM** | Perché modulare, indice di modulazione, regola di Carson, confronto AM/FM, rivelatore di picco, PLL |
| **5 · Laboratorio** | Mappatura reti, analisi dello spettro Wi-Fi, SDR, costruzione di una Yagi; norme di sicurezza; bibliografia |
Elementi didattici:
- **Formule** evidenziate, con esempi numerici svolti.
- **Diagrammi SVG** originali (onde E/B, schema a blocchi della linea, diagrammi di irradiazione, forme d'onda AM/FM).
- **Calcolatori interattivi**: adattamento (ROS, Γ, % di potenza riflessa, Z<sub>T</sub> del trasformatore λ/4) e EIRP (dBW, dBm, W).
- **Verifiche** in forma di domande con risposta nascosta (`<details>`), in ogni sezione.
- Menu che evidenzia la sezione visibile; layout responsive; supporto al tema chiaro/scuro del sistema e alla riduzione del movimento.
## Struttura del repository
```
.
├── index.html   # Struttura e contenuti del sito (pagina unica)
├── style.css    # Stile, tema chiaro/scuro, layout responsive
├── README.md    # Questo file
└── Linee, Antenne e Telecomunicazioni.pptx   # Sorgente didattico originale
```
## Visualizzare in locale
Basta aprire `index.html` in un browser. Per un test più fedele a GitHub Pages, da una cartella del progetto:
```bash
python3 -m http.server 8000
# poi apri http://localhost:8000
```
## Pubblicare su GitHub Pages
1. Crea un repository su GitHub e carica i file (almeno `index.html` e `style.css`).
2. Vai su **Settings → Pages**.
3. In **Build and deployment**, scegli **Source: Deploy from a branch**, poi branch `main` e cartella `/ (root)`.
4. Salva. Dopo un minuto il sito è disponibile su `https://<utente>.github.io/<nome-repository>/`.
Il sito usa solo percorsi relativi (`style.css`, ancore `#sezione`), quindi funziona anche se pubblicato in una sottocartella.
## Note sui contenuti
Durante la trasposizione delle slide sono state fatte alcune precisazioni, utili anche in classe:
- **Dipolo hertziano.** Nella slide 12 è descritto come "struttura simmetrica a mezz'onda". In realtà il dipolo hertziano è un elemento *infinitesimo* usato come modello teorico; il dipolo a mezz'onda (λ/2) è la versione reale. Il sito distingue le due cose.
- **−3 dB.** La slide dice che a −3 dB la potenza scende al 50 %. È corretto. Il campo elettrico, invece, scende al 70,7 % (1/√2).
- **Z₀ non è una resistenza.** È il rapporto tra onde progressive di tensione e corrente. Non si misura con un tester.
- **Immagini.** Le fotografie del file originale (slide 37 riporta gli URL delle fonti) non sono state incluse: il sito usa diagrammi originali in SVG, così non si dipende da risorse esterne né da copyright altrui.
## Fonti
- Presentazione *Linee, Antenne e Telecomunicazioni* (Modulo 5, programma biennale TLC).
- *Manuale di Telecomunicazioni per Istituti Tecnici*, Vol. 2 (come indicato nella presentazione).
- Normative IEEE su irradiazione, modulazioni RF e sicurezza elettromagnetica (come indicato nella presentazione).
## Licenza
Indicare la licenza scelta per il materiale (per esempio CC BY-NC-SA 4.0 per uso didattico). Finché non viene specificata, i diritti restano all'autore.
