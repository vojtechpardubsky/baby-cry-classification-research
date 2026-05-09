# Baby Cry Classification — Research

Experimentální část bakalářské práce zaměřené na automatickou klasifikaci 
dětského pláče pomocí metod strojového učení. Repozitář obsahuje Jupyter 
notebooky, dataset a výstupy experimentů.

Webová aplikace postavená na výsledcích tohoto výzkumu je dostupná v repozitáři
[baby-cry-classification](https://github.com/vojtechpardubsky/baby-cry-classification).

## Struktura repozitáře

```
├── dataset/          # Dataset Donate-a-Cry (WAV soubory)
├── notebooks/        # Jupyter notebooky
│   ├── 0_Ostatni_obrazky.ipynb
│   ├── 3_Dataset_a_analyza_dat.ipynb
│   ├── 4_Predzpracovani_dat.ipynb
│   └── 05_Vysledky_a_evaluace.ipynb
└── outputs/          # Výstupy experimentů
    ├── figures/      # Grafy a vizualizace
    ├── models/       # Natrénované modely
    ├── preprocessed/ # Předzpracovaná data
    └── results/      # Výsledkové tabulky
```
## Obsah notebooků

| Notebook | Popis |
|----------|-------|
| 0 — Ostatní obrázky | Slouží pro tvorbu nadbytečných obrázků mimo kapitoly 3,4 a 5 |
| 3 — Dataset a analýza dat | Explorativní analýza datasetu, distribuce tříd, PCA, t-SNE, k-means |
| 4 — Předzpracování dat | Sjednocení délky signálu, augmentace, extrakce příznaků |
| 5 — Výsledky a evaluace | 27 experimentálních konfigurací, heatmapy, matice záměn |

## Spuštění

### S Conda (doporučeno)

```bash
conda create -n cry-analysis python=3.11
conda activate cry-analysis
pip install -r requirements.txt
jupyter notebook
```

### Bez Conda

```bash
pip install -r requirements.txt
jupyter notebook
```

## Použité technologie

- Python, Jupyter — prostředí pro experimenty
- librosa — extrakce akustických příznaků (MFCC)
- scikit-learn — klasifikační modely (LR, SVM, RF)
- pandas, numpy — zpracování dat
- matplotlib, seaborn — vizualizace

## Licence

MIT License — viz soubor LICENSE.
