# Sturm und Drang e Klassizismus: confronto stilistico

Analisi quantitativa di drammi tedeschi dello Sturm und Drang (SD) e del Klassizismus.

## Struttura del repository

```
Project-work-MasterDH7/
├── Klassizismus/   ← XML dei drammi del Klassizismus
├── SD/             ← XML dei drammi dello Sturm und Drang
├── notebook/       ← .ipynb e .html
├── output/         ← CSV dei risultati
├── LICENSE
└── README.md
```

## Contenuto

- **SD/** e **Klassizismus/**: i testi dei drammi in formato XML, uno per opera (nome file: `autore-titolo.xml`).
- **notebook/**: i notebook Jupyter dell'analisi e la loro versione HTML, leggibile senza eseguire nulla.
- **output/**: tabelle prodotte dall'analisi (distanze Delta, parole distintive, verbi, campi semantici, test di robustezza).

## Come usarlo

1. Scarica o clona il repository.
2. Apri i notebook in `notebook/` e eseguili nell'ordine indicato dal nome.
3. I percorsi sono relativi: i notebook leggono da `../SD/` e `../Klassizismus/` e scrivono in `../output/`.

## Licenza

Vedi il file [LICENSE](LICENSE).
