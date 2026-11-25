# Sturm und Drang e Klassizismus: confronto stilistico

Analisi quantitativa di drammi tedeschi dello Sturm und Drang (SD) e del Klassizismus. Il notebook cerca i lemmi distintivi dei due sottocorpora e verifica che le differenze non dipendano da una singola opera, da un singolo autore o dalla misura statistica scelta.

**Attenzione:** SD e Klassizismus sono qui etichette di due sottocorpora che differiscono insieme per periodo, autori, forma (verso/prosa) ed edizioni. I risultati descrivono differenze lessicali tra i due sottocorpora.

## Struttura del repository

```
Project-work-MasterDH7/
├── Klassizismus/   # XML dei drammi del Klassizismus
├── SD/             # XML dei drammi dello Sturm und Drang
├── notebook/       # Notebook Jupyter (.ipynb) e HTML (.html)
├── output/         # CSV dei risultati
├── requirements.txt    pacchetti Python con le versioni usate
├── LICENSE
├── README.md
└── bibliografia.md
```

I 43 file XML diventano 41 opere nell'analisi, perché le tre parti del Wallenstein di Schiller (`wallensteins-lager`, `die-piccolomini`, `wallensteins-tod`) vengono fuse in un'unica opera.

## Come riprodurre l'analisi

Serve Python 3.9 (l'analisi è stata eseguita con la 3.9.6).

1. Scarica o clona il repository:
   ```bash
   git clone https://github.com/RebZa21/Project-work-MasterDH7
   cd Project-work-MasterDH7
   ```
2. Crea un ambiente virtuale e installa i pacchetti:
   ```bash
   python -m venv .venv
   source .venv/bin/activate        
   pip install -r requirements.txt
   ```
3. Scarica i due modelli linguistici di spaCy (non sono in `requirements.txt`):
   ```bash
   python -m spacy download de_core_news_sm
   python -m spacy download de_core_news_lg
   ```
   Servono le versioni 3.8.0. Versioni diverse possono cambiare la lemmatizzazione e quindi le parole distintive.
4. Apri il notebook:
   ```bash
   jupyter lab notebook/frequenza_relativa_SD_Klassizismus.ipynb
   ```
5. Esegui tutto con *Kernel → Restart Kernel and Run All Cells*.

Il notebook trova da solo le cartelle `SD/` e `Klassizismus/` risalendo dalla cartella in cui è aperto. Se i dati sono altrove, imposta la variabile d'ambiente `GERDRACOR_BASE` con il percorso della cartella che li contiene. I risultati vengono scritti in `output/`.

La prima cella controlla le versioni dei pacchetti e stampa «Ambiente conforme» se coincidono con quelle usate per l'analisi.

## Risultati

In `output/` ci sono le tabelle prodotte dal notebook: frequenze relative, parole distintive per sottocorpus, controlli di robustezza (per opera, per autore, permutazioni), verbi distintivi, contesti, campi semantici, distanze Delta di Burrows, e `config_usata.json` con i parametri dell'esecuzione.

## Dati

I testi sono file TEI scaricati da GerDraCor (https://dracor.org) il <data di download>, in <versione/commit di GerDraCor, se la conosci>. <Condizioni d'uso dei testi: riprendi quanto indicato nell'header TEI dei file.>

## Uso di strumenti di IA

Il codice del notebook è stato sviluppato con l'assistenza di un modello di IA (Claude, Anthropic). La domanda di ricerca, la scelta del corpus e l'interpretazione dei risultati sono dell'autrice.

## Licenza

Il codice è distribuito con licenza Apache 2.0 (vedi [LICENSE](LICENSE)). I testi dei drammi hanno le condizioni indicate al punto «Dati».
