# Struktura adresářů bakalářské práce
Zde je popsána struktura adresářů bakalářské práce včetně jejich obsahu a vysvětlení základního použití.

## Hlavní adresáře:  

### `classes/`  
Obsahuje třídu klasifikátoru a třídu určenou pro zpracováním datasetů.  

- `classifiers.py` – obsahuje klasifikátor ```MainSpeakerIntensity5Classifier(nn.Module)``` sloužící jako konvoluční neuronová síť pro klasifikaci do 5 tříd, nepovinným parametrem inicializace je počet vstupních příznaků. 
- `datasets.py` – obsahuje třídu datasetu ```FeatureDataset(Dataset)``` sloužící pro sekvenční zpracování dat v online režimu při trénování neuronové sítě. Parametry inicializace jsou:
  - adresář s příznaky (*input dir*),
  - adresář s labely (*output_dir*),
  - list obsahující názvy zpracovávaných příznaků, tak jak jsou uloženy v souborech (bez číslovky na konci, včetně podtržítka, *feature_names*),
  - nepovinná hodnota doplňovaných okrajů na počátek a konec nahrávky (*default_padding_value*),
  - nepovinný počet oken nahrávek (*n_frames*, pokud nedoplněn, je automaticky spočítán).

### `data_analysis_scripts/`  
Adresář určený pro skripty a notebooky související s analýzou dat před a po trénování.  

- `comparison_of_pilots.ipynb` – notebook obsahující skripty s výpočtem navrhovaných ideálních pilotních signálů, vyhodnocení extrakce s jejich použitím na trénovacích nahrávkách a jejich vzájemné porovnání za pomoci vizualizace.
- `evaluating_model.ipynb` – notebook obsahující skripty pro vyhodnocení extrakce s použitím vlastních natrénovaných modelů pro tvorbu pilotních signálů na testovacích nahrávkách, jejich vzájemné porovnání za pomoci vizualizace a porovnání vůči referenčním hodnotám (ideálním piloty, slepá a částečně slepá extrakce).
- `iFICA_SIR.ipynb` – notebook obsahující skripty pro vytvoření referenčních hodnot chování algoritmu extrakce na trénovacích nahrávkách v případech kdy pilotní signál je ideální nebo se jedná o slepou či částečně slepou extrakci.

### `data_preprocessing_scripts/`  
Adresář určený pro skripty předzpracovávající data nahrávek do vstupních příznaků sítě a cílových labelů. Více o použití v sekci [trenovani.md](https://github.com/TeVr42/bp_dokumentace/blob/main/trenovani.md). 

- `IPD_preprocessing.ipynb` – notebook sloužící pro předzpracování IPD příznaků dle zadaných parametrů.
- `ILD_preprocessing.ipynb` – notebook sloužící pro předzpracování ILD příznaků dle zadaných parametrů.
- `SIR_pilot_preprocessing.ipynb` – notebook sloužící pro předzpracování cílových pilotních signálů do požadované podoby labelů určených pro neuronovou síť.


### `functions/`  
Obsahuje pomocné funkce a funkci algoritmu informované FICA.  

- `functions.py` – soubor s pomocnými funkcemi využívanými pro různé úlohy napříč zdrojovými kódy.
- `iFICA.py` – funkce pro informovanou rychlou analýzu nezávislých komponent iFICA využívanou pro extrakci.

### `hybrid_systems_scripts/`  
Obsahuje třídu s celým funkčním hybridním systémem a skript s ukázkou jeho použití.

- `hybrid_system.ipynb` – notebook se skripty zobrazující použití celkového hybridního systému pro extrakci hlavního řečníka ze zvukové nahrávky a přehrání extrahovaného signálu.
- `hybrid_system.py` – soubor s třídou představující celkový hybridní systém určený pro extrakci a od ní dědící třídy, které využívají konkrétní natrénované modely.
### `matlab_scripts/`  
Obsahuje soubory s kódy v jazyce Matlab použitými především pro generování dat. Více je jejich použití přiblíženo v souboru [generovani.md](https://github.com/TeVr42/bp_dokumentace/blob/main/generovani.md).

- `generate_dataset.m` – skript určení pro generování smíchaných nahrávek dat pro zadanou situaci.
- `plot_generovani_pozic.m` – skript, který vizualizuje rozložení řečníků a mikrofonů pro zadanou situaci.
- `wsj_data_clean.m` – skript určený pro zpracování WSJ datasetu do formátu využitého při generování - sjednocení názvů a zbavení se opakujících se hodnot.

### `models/`  
Obsahuje natrénované neuronové sítě pro odhad pilotních signálů. Celkem 9 natrénovaných modelů.

- Formát uložení dat je název příznaku (ipd/ild) s dvojicí použitých mikrofonů pro daný příznak (př. 17 - mikrofon 1 a 7) a přípona *model.pt*.

### `results/`  
Obsahuje soubory se srovnáním SIR extrakce s využitím jednotlivých pilotních signálů, originální hodnoty, konečné hodnoty a zlepšení (= finální - zlepšení).

- `SIR_pilots_comp.csv` – tabulka s výslednými hodnotami SIR extrakce pro testované cílové ideální piloty na trénovacích datech.
- `SIR_test.csv` – tabulka s výslednými hodnotami SIR extrakce pro ideální piloty (energie SOI, cílový pilot), referenční piloty (slepé, částečně slepé) a piloty získané s použitím natrénovaných modelů v rámci navrhované metody na testovacích datech.
- `SIR_train.csv` – tabulka s výslednými hodnotami SIR extrakce pro ideální piloty (energie SOI, cílový pilot) a referenční piloty (slepé, částečně slepé) na trénovacích datech.

### `training_scripts/`  
Obsahuje soubor určený pro trénování neuronových sítí pro odhad pilotních signálů dle navrhované metody. Použití je přiblíženo v [trenovani.md](https://github.com/TeVr42/bp_dokumentace/blob/main/trenovani.md).

- `model_training.ipynb` – skript určený pro vlastní trénovaní neuronové sítě. Obsahuje přehledy detailů trénování modelů představených v práci.
