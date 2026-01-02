# Analisi Resilienza Economica Italia: 2019-2025

Analisi comparativa della resilienza economica e occupazionale in Italia, confrontando il periodo pre-pandemia (2019 Q4) con quello post-pandemia (2025 Q3).

## Panoramica del Progetto

Questo progetto analizza oltre **240.000 record** di dati ISTAT per identificare le trasformazioni strutturali dell'economia italiana tra il 2019 e il 2025, con focus su:
- Variazioni occupazionali per settore (classificazione ATECO)
- Performance territoriale delle 20 regioni italiane
- Evoluzione della dimensione media delle imprese
- Identificazione di settori vincenti e perdenti

## Risultati Chiave

### Crescita Nazionale
- **+1.78 milioni** di posti di lavoro (+9.84%)
- **+78.061** unità locali (+1.23%)
- **Consolidamento imprese**: dimensione media da 2.85 a 3.09 addetti/sede (+8.5%)

### Dinamiche Territoriali
- **Sud supera Nord**: Campania +19%, Sicilia +18% vs Lombardia +9.3%
- **Riequilibrio territoriale**: Sud guadagna quota sul PIL nazionale
- **Eterogeneità regionale**: Sud più variabile, Nord più uniforme

### Settori Vincenti
1. **Riparazione Computer/Beni** (+245k addetti, +393%)
2. **Costruzioni Specializzate** (+179k addetti, +18%)
3. **Commercio Dettaglio** (+166k addetti, +8%)
4. **Ristorazione** (+160k addetti, +11%)
5. **Software/IT** (+92k addetti, +32%)

### Settori in Crisi
- Manifattura tradizionale (pelle, tessile, abbigliamento): -6% medio
- Stampa e media: -9%
- Commercio Auto: -100% (anomalia da riclassificazione ATECO)

## Tecnologie Utilizzate

- **Python 3.x**
- **Pandas**: manipolazione e analisi dati
- **NumPy**: calcoli numerici
- **Matplotlib/Seaborn**: visualizzazioni
- **Jupyter Notebook**: ambiente di sviluppo


## Dataset

### Fonti Dati
- **ISTAT**: Registro Statistico delle Imprese Attive (ASIA)
- **Periodo analizzato**: 2019 Q4 (pre-COVID) vs 2025 Q3 (post-pandemia)
- **Granularità**: Provincia, Settore ATECO (fino a 6 cifre)

### Dimensioni Dataset
- **2019 Q4**: 118.814 righe
- **2025 Q3**: 114.591 righe
- **Mappatura ATECO**: 3.157 codici

## Metodologia

### 1. Data Cleaning
- Normalizzazione codici ATECO (rimozione punti, padding zeri)
- Conversione valori numerici
- Gestione valori mancanti
- Pulizia nomi colonne

### 2. Analisi Esplorative
- Aggregazione per settore (88 divisioni ATECO)
- Aggregazione per regione (20 regioni)
- Aggregazione per macro-area (Nord, Centro, Sud)
- Calcolo variazioni assolute e percentuali

### 3. Analisi Avanzate
- Identificazione anomalie (riclassificazioni ATECO 2007→2022)
- Analisi dimensionale imprese (consolidamento vs frammentazione)
- Heatmap specializzazioni territoriali
- Scatter plot crescita vs dimensione
- Box plot distribuzione per area

### 4. Visualizzazioni
Il notebook include oltre 15 grafici professionali:
- Barre orizzontali/verticali per top/bottom settori e regioni
- Grafici a 4 pannelli per confronti Nord-Centro-Sud
- Heatmap per specializzazioni settoriali regionali
- Torte per composizione economia
- Box plot per distribuzioni statistiche
- Dashboard riassuntiva con 6 mini-grafici

## Come Utilizzare

### Prerequisiti
```bash
pip install pandas numpy matplotlib seaborn openpyxl jupyter
```

### Esecuzione
```bash
jupyter notebook Analisi_20192025.ipynb
```

### Output
Eseguendo tutte le celle del notebook verranno generati:
- 8 file CSV con risultati dettagliati
- 1 report esecutivo in formato testo
- 15+ grafici visualizzati nel notebook

## Scoperte e Anomalie

### Riclassificazioni ATECO
Durante l'analisi sono state identificate **riclassificazioni massicce** tra ATECO 2007 e ATECO 2022:

- **Settore Q (Sanità)**: Divisioni 86, 87, 88 migrate fuori dal settore
- **Settore J (ICT)**: Divisioni 61, 62, 63 (telecom, software) migrate verso N
- **Settore M ↔ N**: Scambio di divisioni professionali e supporto imprese
- **Settore 45 (Commercio Auto)**: Completamente riclassificato (-100% apparente)

Queste anomalie **non rappresentano perdite reali** ma cambiamenti metodologici ISTAT.


## Limitazioni

- **Riclassificazioni ATECO**: Alcuni confronti settoriali sono influenzati da cambiamenti metodologici
- **Dati aggregati**: Non disponibili dati a livello di singola impresa
- **Due punti temporali**: Manca l'evoluzione trimestrale 2020-2024
- **Comparabilità**: Necessaria tavola di concordanza ISTAT per confronto omogeneo

## Licenza

Questo progetto è distribuito sotto licenza MIT. I dati utilizzati sono di proprietà ISTAT e soggetti alle loro condizioni d'uso.

