# Knihovna `rasterio` – zpracování rastrových dat v Pythonu

Semestrální projekt zaměřený na představení prostorové knihovny **`rasterio`** a základních postupů práce s geografickými rastry v Pythonu.

## O projektu

Notebook ukazuje hlavní funkce knihovny **`rasterio`** (čtení metadat a georeference, načítání výřezů pomocí `Window`, sjednocování rastrových mřížek funkcí `reproject` a napojení na `NumPy` a `Matplotlib`).

Všechna vstupní data (**Sentinel-2 Level-2A** pro severní část Prahy) se načítají automaticky přes STAC API – není nutné nahrávat žádné vlastní soubory.

## Obsah 

1. **Vyhledání scény a kontrola metadat** (`rasterio.open`, `crs`, `bounds`, `transform`)
2. **Načtení výřezu a kalibrace pásem** (`Window`, `from_bounds`, převod na odrazivost)
3. **Sjednocení prostorového rozlišení** (`reproject`, `Resampling.nearest`)
4. **Vizualizace kompozic** (True Color a False Color / CIR)
5. **Rastrová algebra a maska vegetace** (výpočet indexu NDVI, maskování oblačnosti podle `SCL`, binární maska vegetace)

## Spuštění

Notebook lze spustit přímo v prostředí **Google Colab** bez lokální instalace (všechny potřebné knihovny se nainstalují v první buňce notebooku):

* `rasterio`
* `numpy`
* `matplotlib`
* `pystac-client`
* `planetary-computer`

## Zdroje

* [Dokumentace Rasterio](https://rasterio.readthedocs.io/)
* [Microsoft Planetary Computer – Sentinel-2 L2A](https://planetarycomputer.microsoft.com/dataset/sentinel-2-l2a)
