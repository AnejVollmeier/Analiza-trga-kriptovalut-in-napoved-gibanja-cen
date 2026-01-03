#  Analiza trga kriptovalut in napoved gibanja cen

Projekt za analizo trga kriptovalut z uporabo podatkov iz CoinGecko API-ja.  Projekt vključuje pridobivanje podatkov, analizo trenda in napovedovanje gibanja cen najpomembnejših kriptovalut.

##  Cilj projekta

Cilj projekta je:
- Pridobiti aktualne podatke o TOP 300 kriptovalutah po tržni kapitalizaciji
- Analizirati zgodovinske cenovne trende in volatilnost
- Identificirati korelacije med različnimi kriptovalutami
- Zgraditi napovedni model za kratkoročno gibanje cen

##  Vsebina

Projekt vključuje naslednje analize:

### 1. Pridobivanje podatkov
- Povezava s CoinGecko API
- Pridobivanje podatkov za TOP 300 kriptovalut
- Zbiranje cenovih podatkov in metrik tržne kapitalizacije
- Spremljanje cenovnih sprememb (1h, 24h, 7d, 30d, 1 leto)

### 2. Obdelava podatkov
- Čiščenje in predprocesiranje podatkov
- Obravnava manjkajočih vrednosti
- Normalizacija podatkov
- Priprava podatkov za analizo

### 3. Eksplorativna analiza podatkov (EDA)
- Statistični pregled trga
- Analiza distribucije tržne kapitalizacije
- Analiza volatilnosti in cenovnih nihanj
- Vizualizacija trendov

### 4. Napredne analize
- Korelacijska analiza med kriptovalutami
- Identifikacija vzorcev v gibanju cen
- Analiza volumna trgovanja
- Primerjava performanc različnih kriptovalut

### 5. Napovedni modeli
- Priprava podatkov za strojno učenje
- Gradnja napovednih modelov
- Evaluacija in primerjava modelov
- Napovedi prihodnjih cenovnih gibanj

##  Tehnologije

Projekt uporablja naslednje Python knjižnice: 

```python
- pandas              # Obdelava podatkov
- numpy              # Numerične operacije
- matplotlib         # Vizualizacija
- seaborn           # Napredne vizualizacije
- requests          # API klici
- scikit-learn      # Strojno učenje
- statsmodels       # Statistične analize
```

##  Podatkovni viri

**CoinGecko API** - Brezplačen API za podatke o kriptovalutah: 
- Endpoint: `https://api.coingecko.com/api/v3/coins/markets`
- Parametri: EUR valuta, razvrstitev po tržni kapitalizaciji
- Frekvenca:  Pridobivanje podatkov z 2-sekundnim zamikom med zahtevki
- Omejitve: Brezplačni plan omogoča omejeno število zahtevkov na minuto

##  Uporaba

### Predpogoji

```bash
pip install pandas numpy matplotlib seaborn requests scikit-learn
```

### Zagon projekta

1. Klonirajte repozitorij:
```bash
git clone https://github.com/AnejVollmeier/Analiza-trga-kriptovalut-in-napoved-gibanja-cen.git
cd Analiza-trga-kriptovalut-in-napoved-gibanja-cen
```

2. Odprite Jupyter Notebook:
```bash
jupyter notebook Kriptovalute_Anej_Vollmeier.ipynb
```

3. Zaženite celice po vrsti za: 
   - Pridobivanje podatkov
   - Analizo trga
   - Vizualizacijo rezultatov
   - Gradnjo napovednih modelov

### Google Colab

Projekt lahko zaženete tudi v Google Colab brez lokalne namestitve:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge. svg)](https://colab.research.google.com/github/AnejVollmeier/Analiza-trga-kriptovalut-in-napoved-gibanja-cen/blob/main/Kriptovalute_Anej_Vollmeier.ipynb)

## 📈 Zbrani podatki

Za vsako kriptovaluto projekt zbira: 

| Parameter | Opis |
|-----------|------|
| `id` | Unikatni identifikator |
| `symbol` | Kratica (npr. BTC, ETH) |
| `name` | Polno ime |
| `market_cap_rank` | Rang po tržni kapitalizaciji |
| `market_cap` | Tržna kapitalizacija v EUR |
| `fully_diluted_valuation` | Popolnoma razredčena vrednost |
| `current_price` | Trenutna cena v EUR |
| `total_volume` | Skupni volumen trgovanja |
| `high_24h` / `low_24h` | Najvišja/najnižja cena v 24h |
| `price_change_percentage_*` | Cenovna sprememba (1h, 24h, 7d, 30d, 1y) |

##  Struktura projekta

```
Analiza-trga-kriptovalut-in-napoved-gibanja-cen/
│
├── Kriptovalute_Anej_Vollmeier.ipynb    # Glavni notebook
├── coingecko_kriptovalute.csv           # Podatki (generira se avtomatsko)
├── README.md                             # Ta dokument
└── . gitignore                            # Git ignore datoteka
```

##  Opozorila

- **API omejitve**: CoinGecko brezplačni API ima omejitve hitrosti.  Skript vključuje 2-sekundne zamike med zahtevki.
- **Podatki v realnem času**: Podatki so snapshot trenutnega stanja trga in se spreminjajo.
- **Investicijsko svetovanje**: Ta projekt je izključno za izobraževalne namene in NI investicijsko svetovanje.

##  Avtorstvo

**Anej Vollmeier**

- GitHub: [@AnejVollmeier](https://github.com/AnejVollmeier)
- Projekt: [Analiza trga kriptovalut](https://github.com/AnejVollmeier/Analiza-trga-kriptovalut-in-napoved-gibanja-cen)
