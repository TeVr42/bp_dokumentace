# Testování fungování hybridního systému pro extrakci

Způsob testování netrénovaných modelů a porovnání s referenčními hodnotami extrakce s ideálními či slepými piloty je viditelný v souboru `data_analysis_scripts/evaluating_model.ipynb`. Následující části popisují postup, jak případně spustit vlastní trénování v daném souboru.

## Úvodní nastavení
Pokud jste dosud nestáhli obsah repozitáře:
1. Stáněte obsah repozitáře bakalářské práce do vybaného adresáře.
2. Nainstalujte potřebné knihovny Pythonu, ideálně do vytvořeného virtuálního prostředí (například dle souboru **requirements.txt** ```pip install -r requirements.txt```).
3. Vytvořte soubor **data** na úrovni hlavního hlavního adresáře, do něj vytvořte soubor **test**, do kterého nakopírujte vygenerované soubory s nahrávkami vytvořenými dle návodu [generovani.md](https://github.com/TeVr42/bp_dokumentace/blob/main/generovani.md) (soubory s*.wav a y*.wav).

Po úspěšné přípravě dat a instalaci potřebných knihoven pokračujte v souboru `data_analysis_scripts/evaluating_model.ipynb`:
1. Spusťte první buňku souboru s potřebnými importy, buňka po úspěšném proběhnutí bude ukazovat symvol *Success*.
2. V následující druhé buňce upravte počet nahrávek ```number_of_samples = 600```, dle Vámi vybraného počtu. Následně buňku spusťtě.

## Spočítání referenčních hodnot SIR extrakce
1. Spusťte buňku s definicí funkce ```get_SIR_for_basic_pilots(number_of_samples)```.
2. Spusťte výpočet referenčních hodnot pomocí ```SIR_df = get_SIR_for_basic_pilots(number_of_samples)```. Výsledkem je tabulka s hodnotami uložená v proměnné ```SIR_df```.
3. Tabulku uložte pomocí ```SIR_df.to_csv('../results/SIR_test.csv', index=True)```.


## Spočítání hodnot SIR extrakce s natrénovanými modely
1. Spusťte buňku s definicí funkce ```get_improvement_for_hybrid_system(hybrid_system, number_of_samples)```.
...

