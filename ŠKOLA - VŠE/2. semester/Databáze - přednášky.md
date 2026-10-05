## Cvičení 17.02.2026
*konzultace nejsou problém, není na budově, připravit si problém, psát mu*
**test během semestru*, můžu se omluvit ale pak píšu 2 testy najednou ve zkouškovém*
- dokumentový strom

---
## Přednáška 19.02.2026
- [Odkaz na první prezentaci](file:///Users/boris/VS%CC%8CE/databa%CC%81ze/4IT218_2026_LS_predn_01.pdf)
- **certifikáty z datacampu** přidávají **5** bonusových **bodů** - tldr když budu mít 10 bodů z testu dostanu 15 když to předložím
- 15.05.2026 23:59 - **odevzdat dokumentaci** i databázy plnou dat jinak autom loose 40 bodů
- pilotní kurz na grafické databáze -> absolvování = 5 bodů
## Přednáška 26.02.2026
- vypiš mi oddelění kde není zařazený žádný zaměstanec či co, tak tam se ne vždy vyplatí join a podmínkou
	- vypište čísla a názvy oddělení, ve kterých nepracuje žádný ing (použitím vnořených dotazů)
```sql
select cis_odd, nazev from oddel where cis_odd not in(select distinct cis_odd from zam where titul = 'ING';);
```

## 05.03.2026
[prezentace lol](file:///Users/boris/VS%CC%8CE/databa%CC%81ze/pr%CC%8Cedna%CC%81s%CC%8Cky/4IT218_2026_LS_predn_03.pdf)

- base tables - tabůlky které bez kterých se databáze neobejde
- odvozené - snapshot tabulky (statické) *VIEW
	- dynamické odvozené tabůlku (View)
		- je to databázový objekt -  je to jenom průhled do databáze
			- pro zpřístupnění databáze veřejným uživatelům - a dat jim práva jenom na to view ať mi nemůžou šahat na to co nemají
			- můžeme filtrovat co chceme ukoazovat
- dočasné tabulky
	- každý select je dělá

zajištění, aby každá hodnota atributu byla v souladu s množinou přípustných hodnot.
podpora v SQL:
-  odvozený z domény
- vlastnost objektu z nějakého svět který bsahuje
- od SQL89 klauzule CHECK (Příklad: PLAT NUMBER(10,2) check (PLAT between 100 and 60000)
- od SQL92 CREATE DOMAIN (Příklad: create domain PLATDOM NUMBER(10,2) check PLATDOM between 100 and 60000; v příkazu create table zam pak u sloupce PLAT uveden odkaz na doménu: PLAT PLATDOM)

CREATE TABLE - INTEGRITNÍ OMEZENÍ
2. Entitni integrita
- zajisten jednoznané identifikace kazdého radku relaini tabulky.
- podpora v SQL:
- od SQL86 pouzes pouzitim kombinace klicovych slovy UNIQUE a NOT NULL (Priklad: create table ZAM ( CIS INTEGER unique not null)
- od SQL89 PRIMARY KEY (Priklad: create table ZAM (CIS INTEGER primary key, ...)

## 12.03.2026
[přednáška č.4](file:///Users/boris/VS%CC%8CE/databa%CC%81ze/pr%CC%8Cedna%CC%81s%CC%8Cky/4IT218_2026_LS_predn_04.pdf)

## 19.03.2026
[přednáška č.5](file:///Users/boris/VS%CC%8CE/databa%CC%81ze/pr%CC%8Cedna%CC%81s%CC%8Cky/4IT218_2026_LS_predn_05.pdf)

- problém s homonymy, datum dodání? atd... a synonymy - jasně a čistě vše jmenovat
---
příklad *čsfd*

## 26.03.2026
[přednáška č.6](file:///Users/boris/VS%CC%8CE/databa%CC%81ze/pr%CC%8Cedna%CC%81s%CC%8Cky/4IT218_2026_LS_predn_06.pdf)

5 úrovní normalizace databáze
atomizace a....

## 16.04.2026
[prezentace č.9t](file:///Users/boris/VS%CC%8CE/databa%CC%81ze/pr%CC%8Cedna%CC%81s%CC%8Cky/4IT218_2026_LS_predn_09.pdf)

OLTP vs OLAP databázová zpracování
- předpočítání dotazů třeba

## 23.04.2026
[přednáška č.10](file:///Users/boris/VS%CC%8CE/databa%CC%81ze/pr%CC%8Cedna%CC%81s%CC%8Cky/4IT218_2026_LS_predn_10.pdf)

