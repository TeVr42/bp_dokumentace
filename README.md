Dokumentace k realizaci bakalářské práce

Tento repozitář slouží jako technická a zároveň doplňující dokumentace k bakalářské práci s názvem:

Hybridní systém pro extrakci řečového signálu na základě informovaném algoritmu FICA
Autor: Tereza Vrbová
Vedoucí práce: prof. Ing. Zbyněk Koldovský, Ph.D.

Hlavním cílem této dokumentace je poskytnout komplexní přehled o softwarové části bakalářské práce, a to jak z hlediska struktury kódu, tak i z pohledu samotné implementace jednotlivých komponent celého navrženého systému. Dokumentace by měla čtenáři umožnit hlubší porozumění nejen samotnému algoritmu FICA a jeho implementaci, ale také celému podpůrnému ekosystému, který byl v rámci práce vytvořen – od generování syntetických dat až po testování a vyhodnocení výsledků.
Obsah a struktura dokumentace

Tato dokumentace je rozdělena do několika částí, přičemž každá z nich se věnuje konkrétnímu aspektu práce. Dokumentace má sloužit nejen jako praktický návod k použití jednotlivých skriptů, ale i jako podklad k porozumění tomu, jak byly jednotlivé kroky realizovány a jak spolu vzájemně souvisejí.
Hlavní části dokumentace:

    Struktura adresářů – podrobný popis jednotlivých složek, jejich účelu a obsahu. Tento popis je uveden v souboru struktura.md. Uživatel zde najde přehled hlavních komponent systému, včetně pomocných skriptů, trénovacích dat, modelů a výstupů.

    Generování syntetických nahrávek – podrobný návod, jak vygenerovat vlastní syntetická data, která slouží jako vstup pro testování navrženého systému. Tento proces je popsán v souboru generovani.md a zahrnuje i informace o parametrech, které lze při generování měnit.

    Trénování neuronové sítě – detailní postup, jak natrénovat neuronovou síť, která slouží k získání tzv. postranní informace nezbytné pro správné fungování hybridního systému. Tento postup je popsán v dokumentu trenovani.md, který zahrnuje i informace o použitých architekturách, optimalizačních strategiích a doporučených hyperparametrech.

    Testování a vyhodnocení systému – návod, jak provést otestování celého hybridního systému na připravených syntetických datech. Tento návod je uveden v souboru testovani.md a obsahuje i návrh metrik, které lze při vyhodnocování použít.

Technické specifikace a požadavky na prostředí

Všechny skripty a kódy byly implementovány v jazycích Python (verze 3.12.4) a MATLAB (verze R2025a). Pythonové části jsou navrženy modulárně a využívají řadu knihoven pro práci s daty, zpracování audia a strojové učení. Kompletní seznam použitých Python knihoven, včetně jejich konkrétních verzí, je uveden v souboru requirements.txt.

Kód je připraven tak, aby byl co nejsnáze znovu použitelný a přenositelný. Doporučuje se pracovat ve virtuálním prostředí (např. pomocí venv nebo conda), čímž je zajištěna kompatibilita verzí a bezproblémové spuštění skriptů i na jiných strojích.
Cílová skupina této dokumentace

Dokumentace je určena především čtenářům samotné bakalářské práce, kteří mají zájem o hlubší porozumění implementačním detailům. Zejména ji tedy ocení:

    Vedoucí práce, který zde může získat přehled o kvalitě technického řešení a metodické správnosti přístupu.

    Oponent práce, kterému dokumentace usnadní orientaci v předloženém kódu a poskytne podpůrné materiály k posouzení kvality a originality provedení.

    Hodnotící komise, která může využít dokumentaci pro lepší porozumění tomu, jak teoretické poznatky byly převedeny do praxe.

    Další zájemci o danou problematiku, například studenti, výzkumníci nebo vývojáři, kteří by rádi systém replikovali, upravili či dále rozvíjeli.

