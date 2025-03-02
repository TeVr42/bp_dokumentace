# Trénování CNN modelu pro tvorbu pilotního signálu
Zde je popsán postup vlastního trénování modelu krok za krokem, jeho následné použítí je přiblíženo v souboru testovani.md

1. Stáněte obsah repozitáře bakalářské práce do vybaného adresáře
2. Nainstalujte potřebné knihovny Pythonu, ideálně do vytvořeného virtuálního prostředí (například dle souboru **requirements.txt** ```pip install -r requirements.txt```)
3. Vytvořte soubor **data** na úrovni hlavního hlavního adresáře, do něj vytvořte soubor **train** (a případně **test**), do kterého nakopírujte vygenerované soubory s nahrávkami vytvořenými dle návodu **generovani.md** (soubory s*.wav a y*.wav)
4. Vytvořte soubor **preprocessed_data** na úrovni hlavního hlavního adresáře se soubory práce
5. Otevřete adresář **scripts_data_preprocessing**
  - Předzpracujte příznaky: 
  - Otevřete soubor **ILD_preprocessing.ipynb** pro předzpracování ILD příznaků nebo **ILD_preprocessing.ipynb** pro IPD příznaky
  - Spusťte úvodní buňku s importy
  - Spusťtě buňku s definicí funkce ```preprocess_data(number_of_data, name, mic1, mic2)```
  - Spusťte vybranou bunku pro předzpracování nebo vytvořte novou dle požadavků, jako parametry uveďte počet zpracovávaných dat (number_of_data, maximálně celkový počet vámi vygenerovaných dat), požadovaný název nově vytvářených příznaků (name) a čísla mikrofonů, ze kterých má být daný příznak generován (mic1 a mic2, možnosti jsou v rozsahu 0-8 začínající horní řadou a končící dolní řadou mikrofonů)
  - Otevřete soubor **SIR_pilot_preprocessing.ipynb**
  - Spusťtě úvodní buňku s importy a buňku s definicí funkce ```preprocess_data(number_of_data)```
  - Spusťtě buňku s příkazem preprocess_data pro vybraný počet zpracovávaných nahrávek (obdobný jako u příznaků)
6.
