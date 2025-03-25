# Dokumentace k realizaci bakalářské práce

Tento repozitář slouží jako technická, podrobná a doplňující dokumentace k bakalářské práci s názvem:

**Hybridní systém pro extrakci řečového signálu na základě informovaného algoritmu FICA**  
**Autor:** Tereza Vrbová  
**Vedoucí práce:** prof. Ing. Zbyněk Koldovský, Ph.D.

## Úclem dokumentace

Cílem tohoto dokumentu je poskytnout ucelený, srozumitelný a praktický pohled na softwarovou implementaci bakalářské práce, její strukturu a způsob použití. Dokumentace je určena jak pro čtenáře bakalářské práce, tak i pro uživatele, kteří se zajímají o praktické aspekty realizace hybridního algoritmu FICA, a chtějí porozumět jednotlivým krokům implementace, a případně sami replikovat nebo upravovat dané řešení.

Repozitář obsahuje jak zdrojové kódy, tak pomocné soubory a podrobnou dokumentaci, která krok po kroku vysvětluje logiku a princip fungování celého navrženého systému.

## Obsah dokumentace

Dokumentace je rozdělena do několika tematických sekcí, které společně tvoří celek a navzájem na sebe navazují:

### 1. Struktura adresářů

V dokumentu `struktura.md` je podrobně popsána struktura adresářů a jednotlivých souborů v repozitáři. Popisuje, kde se nachází zdrojové kódy, trénovací data, uložené modely, vstupní a výstupní soubory, pomocné skripty a jak spolu jednotlivé komponenty souvisejí. Tato část slouží jako výchozí bod pro orientaci v projektu.

### 2. Generování syntetických dat

V dokumentu `generovani.md` je uveden kompletní návod, jak vygenerovat syntetická řečová data, která jsou následně využita při testování navrženého algoritmu. Jsou zde popsány používané parametry, datové formáty, struktura vstupních nahrávek, a také postup, jak měnit vlastnosti generovaných signálů podle požadavků testovacích scenářů.

### 3. Trénink neuronové sítě

V souboru `trenovani.md` je detailně popsán proces trénování neuronové sítě, která slouží k extrakci postranní informace nezbytné pro správné fungování hybridního modelu. Popis zahrnuje použité datové sady, architekturu sítě, použité knihovny, parametry trénování, optimalizační metody, a také ukázky vyhodnocení trénovacího procesu.

### 4. Použití hybridního modelu

V dokumentu `testovani.md` je popsán způsob, jak provést testování a validaci celého navrženého hybridního modelu. Jsou zde vysvětleny vstupy, očekávané výstupy, a používané metriky pro vyhodnocení kvality separace řečového signálu. Tato část umožňuje jednoduše ověřit, zda implementace funguje správně a jaké jsou její přínosy.

## Technické specifikace

Implementace jednotlivých komponent byla provedena v programovacích jazycích **Python (verze 3.12.4)** a **MATLAB (verze R2025a)**. Pro Pythonovou část byly použity knihovny jako `numpy`, `scipy`, `librosa`, `pytorch` a další, jejichž seznam včetně verzí je uveden v souboru `requirements.txt`. 

Pro MATLAB byly využity vestavěné funkce a toolboxy pro zpracování signálů. Důležitá byla také kompatibilita mezi formáty dat sdílených mezi Pythonem a MATLABem, která byla zajištěna pomocí souborů ve formátech `.mat` a `.npy`.

Důraz byl kladen na čistotu kódu, modularitu a přehlednost, takže jednotlivé skripty jsou jasně odděleny podle účelu a lze je spouštět nezávisle.

## Cílová skupina dokumentace

Tato dokumentace je určena:

- **Vedoucímu bakalářské práce**, pro lepší porozumění detailům praktické realizace navržené metody.
- **Oponentovi práce**, který může na základě těchto podkladů posoudit technickou úroveň zpracování.
- **Hodnotící komisi**, která si může udělat přesnější obraz o implementační stránce práce.
- **Budoucím studentům a výzkumníkům**, kteří mohou tuto práci použít jako inspiraci nebo výchozí bod pro další výzkum.

---

V případě jakýchkoli dotazů ke kódu, nejasnostem v použití nebo návrhům na vylepšení, kontaktujte autora práce.

Děkujeme za použití tohoto repozitáře a zájem o danou problematiku.
