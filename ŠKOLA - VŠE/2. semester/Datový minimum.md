## 31.03.2026 - cv 1
petr.wolf@vse.cz
konzultace: MS Teams - externista

Hodnocení:
- Týmová analýza v Excelu - 30 b
- Týmová analýza v power bi - 30 b
- Závěrečná prezentace - 30 b
	- kvalita atd...
- Kontrolní testy během cvičení - 10 b
---
### Cviční 01
[úvodní prezentace](https://vse.sharepoint.com/:p:/r/sites/teams-32519/_layouts/15/Doc2.aspx?action=edit&sourcedoc=%7B4c4ee0b0-0f1c-48cd-a472-1391c986e23a%7D&wdExp=TEAMS-TREATMENT&web=1)
[první cvičení - prezentace](https://vse.sharepoint.com/:p:/r/sites/teams-32519/_layouts/15/Doc2.aspx?action=edit&sourcedoc=%7B2c517558-399b-44e7-87fa-3946addb3b42%7D&wdExp=TEAMS-TREATMENT&web=1)

#### Popsi hry:

obyvatelé mají peníze a preferenece a potřebuji *jídlo* - senzitivita na reklamu
 - textová hra
 - z dat který hra generuje
 - **Cíl** vytvořit si vlastní restauraci a vydělat co nejvíce peněz
	 - investovat do reklamy, kampaně - v jaké části města promovat
- Vybrat produkt, který budete prodávat​    

- V rámci kategorie​
	- Určité kvality​
	- Za jakou cenu​
- Stanovit marketingovou kampaň, kterou zaujmete zákazníky​
	- Forma kampaně (banner, hostesky aj.)​
	- V jaké části města (např. předměstí nebo centrum)​
	- V jaký čas (den + část dne – ráno/odpoledne/večer) ​

[hra](https://adgame.vse.cz/#/join)

## 14.04.2026 - cv 2
kontingenční tabulky

- Účinnost - odhalení poznatků
- Rychlost - velmi rychlé na velké množiny
- Přesnost - redekují lidské chyby
- Felxibilita - změna pohledů na data okamžitě

⌘+T vytvoří z dat tabulku
Pivot tables

## 28.04.2026 - dimenzionální modelování
- základní logika uložení a uspořádání dat, tak aby vyhovovalo požadavkům
	- snadná analytická manipulace
	- vysoký výkon
	- ---- vs excel
		- excel a jeho omezení:
		- počet řádků, přidávání dalších atributů
		- ruchlost a paměť nejsou optimální
		- pouze jednoduché kalkulace

- Analytická síla modelu = granularita (větší detail = další tabulka / více řádku-sloupců)

Co je dimenze
- analytické hledisko pro hodnocení ukazatelů
- umožňuje analýzu dat z určitého pohledu
- slouží k popisu sledované skutečnosti (faktů)
- skládá se z prvků
- obvykle hierarchická struktura

Proč dimenzování
- organizace dat pro potřeby
- S dimenzionálním modelem můžeme:
	- načíst několik tabulek do jednoho modelu
	- nastavit vztahy mezi tabulkami
	- využít SQL / DAX a další

- Zdrovojá databáze (OLTP)
	- transakce
- ->
- ETL (extract, transform, load)
- ->
- Analytická databáze (OLAP)
	- analýzy

Datová kvalita
	= vlastnost dat určující do jaké míry naplňují požadavky
- Charakteristiky DQ
	- úplnost
	- přesnost
	- konzistence
	- dostupnost
	- aktuálnost (často se nemažou stará data z důvodu historické analýzy)
	- platnost
	- ...
- činnost pro zajištění DQ: profilování, čištění, stsandardizace, validace
- Data Quality Management (DQM)

Fakta a dimenze
- fakta / metriky / ukazatele = něco, co se stalo - skutečnost
- dimenze = něco, co popisuje skutečnost

## 05.05.2026

