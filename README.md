# Dokumentace k realizaci bakalářské práce
Tento repozitář slouží jako technická dokumentace k bakalářské práci:

**Hybridní systém pro extrakci řečového signálu na základě informovaném algoritmu FICA** 
<br> autor: Tereza Vrbová, vedoucí práce: prof. Ing. Zbyněk Koldovský, Ph.D.

Repozitář poskytuje orientaci v kódech vytvořených v rámci této práce a způsob jejich použití.

Obecně se práce zabývá problémem extrakce řečového signálu hlavního řečníka stojícího ve vybrané oblasti v hlučném prostředí s jinými řečníky. Kódy práce obsahují finální software pro extrakci, skripty sloužící pro vyhodnocení extrakce a analýzu problémů a skripty určené pro trénování neuronových sítí vyvíjených v rámci práce.

## Obsah dokumentace:
Dokumentace přibližuje strukturu adresářů a fungování jednotlivých kódů, slouží pro seznámení s realizací práce.

* **Struktura adresářů** je přiblížena v dokumentu: [struktura.md](https://github.com/TeVr42/bp_dokumentace/blob/main/struktura.md)
* Postup **vygenerování vlastních sysntetických nahrávek** je přiblížen v dokumentu: [generovani.md](https://github.com/TeVr42/bp_dokumentace/blob/main/generovani.md)
* Postup **trénování vlastní neuronové sítě** pro zisk postranní informace je přiblížen v dokumentu: [trenovani.md](https://github.com/TeVr42/bp_dokumentace/blob/main/trenovani.md)
* Způsob **použití hybridního systému** na syntetických datech pro ověření fungování je popsán v souboru: [testovani.md](https://github.com/TeVr42/bp_dokumentace/blob/main/testovani.md)

## Technické specifikace:
Kódy práce jsou vyhotoveny za pomoci programovacích jazyků Python (3.12.4) a Matlab (R2025a). Konkrétní použité knihovny jazyka Python včetně verzí jsou uvedeny v souboru *requirements.txt*.

## Pro koho je dokumentace určena?
Tato dokumentace je určena především čtenářům bakalářské práce, kteří se zajímají i o její konkrétní realizaci, především tedy vedoucímu práce, oponentovi práce a případně hodnotící komisi.
