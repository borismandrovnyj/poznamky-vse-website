## Přednáška 18.02.2026
### Instance
- také jako objekt
- třída je předpis, jak má vypadat instance
- instance třídy auto - auto které vidím na ulici
- třída popisuje jak se má instance chovat
	- instance provádí dané chování
- abstraktní reality
###  Datové atributy
- vlastnosti konkrétní instance
- každá instance v nich má uložena informace
	- například barva
###  Metody
- schopnosti tříd
- vykonávat nějakou operaci s danou instancí
	- příkald: auto umí jezdit a zastavit
### Vytvoření instance
- konstruktor
- je speciální typ metody, pouze k vytvoření nové instance
### Konstrukce třídy
#### Třída
- obyčejný textový soubor .java
- třída začíná slovem public/private/protected
	- následuje slovo class - definice třídy
	- další jméno třídy - stejné jako název souboru
		- Auto.java
- Tělo třídy (místo kam se píší datové atributy a metody)
	- Začíná znakem {a končí znakem}
	- Veškeré věci musí být napsaný mezi těmito závorkami
#### Datové atributy
- slouží k uložení informací o instanci
- píší se do horní části třídy
- datový atribut typicky začíná slovem private/protected/public
	- datový typ
	- název
- jméno - unikátní identifikátor
- určení typu a názvu = deklarace
- do dat. atribut. je také možné nastavit počáteční hodnotu
	- = inicializace
#### Identifikátor
- posloupnost písmen, číslič, podtržítek
	- začíná pismenem
- Java rolišuje malá a velká písmena
	- ciso x Cislo
- Používáme pro pojmenování
	- tříd
	- datových atributů
	- metod
	- lokálních proměnných
	- parametrů
	- ...
- by měl vystihovat obsah toho co pojmenovává
	- metody často sloveso
		- "vypocitejCislo", "zastavit"
- Pro vše ostatní se časot používají podstatná jména
	- "Auto", "druhAuta"
#### Jmenné konvence
- velké písmeno na začátku
	- camel nameing convention
		- každé nové slovo velké písmeno
		- "NakladniAuto"
- Malé písmeno na začátku
	- Všechna počáteční písmena nového slova velká
	- pouížívá se pro jména
		- datových atributů a proměnných
		- metody
		- parametry
- Všechna velká písmena
	- jednotlivá slova oddelěná pomocí _
	- používá se POUZE u konstant
	- "MOJE_KONSTANTA"
#### Metody
- Jedná se o dovednost či činnost
- metody jsou vytvářeny (deklarovány) ve spodní části třídy
- Metoda se skládá z
	- hlavičky (popisu) metody
	- Těla metody, které je tvořeno pomocí
		- příkazu
		- deklarací lokálních proměnných
- typicky slovem public
- následuje návratový typ metody
	- něco co nám metoda dá po spuštění/zavolání
	- pokud metoda nemá nic produkovat/vracet, uvedeme zde void
- Další následuje jméno
- Za jménem metody jsou vždy () následované tělem metody
	- do těchto závorek se umisťují parametry metody
- tělo metody
	- začíná { a končí }
	- nemůžeme zde psát další metody či tvořit datové atributy
- většina příkazů, které do těla umístíme končí ';'
#### Volání metody
- se myslí její použitá na instanci
- například
	- představme si, že máme vytvořenou instanci našeho auta
	- pokud chceme získat získat rok výroby našeho auta, musíme použít (zavolat) metodu getRokVyroby
		- `mojeAuto.getRokVyroby();`
#### Parametry metody
- Slouží k předání vstupních hodnot do metody
	- Jinak řečeno, jsou to hodnoty, bey kterých metoda nemůže pracovat
	- Například metoda "secti", bude mít 2 číselné parametry, jinak by nebylo jasné, jaké čísla se mají sečíst
- Každý  parametr je v hlavičce deklarována poobně jako datové atributy -> typem a jménem
- Modifikátor přístup neuvádí
- Není možné přiřadit parametru implicitní hodnotu
- Pokud má metoda více parametrů, jsou odděleny čárkou
#### Lokální proměnná
- druh proměnné podobně jako datový parametr
- existuje pouze po dobu běhu metody
	- po ukončení metody končí život proměnné
- slouží k ukládání mezivýsledků
- neuvádíme modifikátory přístupu
- podobné parametru metody, ale nemusí být uvedena v hlavičce (ale lepší do hlavy)
#### Obsah metody
- volání jiných metod
- přiřazování do lokálních proměnných a datových atributů
- sekvence
- selekce (rozhodování)
- iterace (loopy)
- příkaz ukončení cyklu
#### Konstruktor
- musí se vždy jmenovata jako třída
- nemá návratný typ
- pokud není expkcitině udělána je automaticky vytvořena - viz. defaultní hodnoty dat. typů wiki
- může být jich vícero
	- liší se v typech a množství parametrů
- obvykle se dává mezi parametry a metody
#### Vytvoření instance
- konstruktor se volá "new"
- vytvořenou instanci musíme uložit do proměnné, aby se s ní dalo pracovat
	- `Auto mojeAuto = new Auto();`
## 25.02.2026
Aritmetické operátory
- **+=**
- **-=**
- **/=**
- **\*=**
- x++
	- nejprve se použije x a pak se přičte
		- `vysledek = x++; //=10`
- ++x
	- nejprve se přičte a pak se zapíše
		- `vysledek = ++x; //=11`
- podíl 2 cellých čísel = celočíselné dělení tudíž 5/2
	- proto musíme psát 5d/2 nebo 5.0/2 = 2.5
- x/0 v cellých číslech = chyba
	- pokud double = ∞
#### Přetypování
Z menší na větší - není problém
- `byte maleCislo = 10;`
- `long velkeCislo = maleCislo;`
- `double desetinne = velkeCislo;`
pokud je číslo třeba moc veliké, tak ale musíme udělat jinak - Z většího na menší
- `long velkeCislo = 10;`
- `int mensiCislo = (int) velkeCislo;`
Přetypování referenčních typů
	- `Objekt auto = new Auto("škoda");`
	- `Auto mojeAuto = (Auto) auto; //ale musí být potomkem`
Operátory pro objekty
- .
- == a != porovnávají odkazy v paměti
- ```java
	 `Auto auto1 = new Auto("Škoda");`
	 `Auto auto2 = auto1;`
	 `Auto auto3 = new Auto("Škoda");`
	 `auto1 == auto2 ;//true`
	 `auto1 == auto3; //false`
	 `auto1.equals(auto3); true`	  
	```
- instanceOf
- ```java
	 `Object auto = new Auto("Škoda");`
	 `boolean jeAuto = auto instanceOf Auto;`  
	```
- class operátor
	- vrátí instanci speciální třídy
- String + String = StringString

#### Zapouzdření
- skrytí interního stavu objektu před zbytkem aplikace
	- private/protected - přístupový modifikátor
		- metody pro přístup - getter & setter

## 04.03.2026
Interface - jazyková konstrukce
šablona pro třídy viz prezentace
[prezentce 3. přednáška](file:///Users/boris/VS%CC%8CE/programova%CC%81ni%CC%81/Pr%CC%8Cedna%CC%81s%CC%8Cka%203.pdf)
## 11.03.2026
[přednáška č.4](file:///Users/boris/VS%CC%8CE/programova%CC%81ni%CC%81/Pr%CC%8Cedna%CC%81s%CC%8Cka%204.pdf)
- pokud jsi jsou rovny na základě equals tak musí být rovny na základě hasCode
	- nemusí si být rovny přes equals, jestliže jsou rovny skrze hashCode
- Kolekce – Collection
	- Seznam – List
	- Množina – Set
	- Fronta – Queue
	- Pole – Array •
		- Jednorozměrná
		- Vícerozměrná 
	-  Mapa – Map
	- Výčtový typ – Enum 
```java
Collection<generickýTyp> mojeAuta;
```
- collection je interface
 ![[Pasted image 20260311151935.png|442]]
- metody
	- add
	- contains
	- empty
	- size
	- remove
	- clear¨
**List - (nejčastěji ArrayList)**
- může obsahovat duplicitní záznamy
- indexová struktura od 0 až po n

```java
List<Auto> seznamAut = new ArrayList<Auto>();
List<Auto> seznamAut = new ArrayList<>();        //to stejný
ArrayList<Auto> seznamAut = new ArrayList<>();   //to stejný
```
- list nefunguje pro primitivní datové typy, ošem dá se obejít obavolým typem - třídou toho typu, kde int - Integar, double - Double...
- metody
	- add(index, element)
	- get(index)
	- remove(index)
	- remove(matching expression)
		- myšleno jestli je "kun", tak remove(kun) odebere kun a nemusím psát konkrétní č.
		- odstraní to ovšem první výskyt hodnoty "kun" a ostatní zůstanou
			- removeAll()
**Set**
- neumožňuje duplicitní záznamy
- nedrží pořadí uložení
- pro přístup k hodnotám neumožňují indexy
- když potřebujeme **custom objekty** v setu, tak potřebujeme do třídy implementovat hashCode a equals - vygenerování přes ideau, ale je to potřeba jinak *Set* si bude myslet
![[Pasted image 20260311154159.png|363]]
## 18.03.2026
[skibid prezentace č.5](file:///Users/boris/VS%CC%8CE/programova%CC%81ni%CC%81/Pr%CC%8Cedna%CC%81s%CC%8Cka%205.pdf)

vararg:
![[Pasted image 20260318150725.png|346]]
- nepovinný parametr v metodě, vždycky to je poslední parametr
	- tento nepovinný parametr funguje jako pole, můžu tudíž do něj psát n čísel
	![[Pasted image 20260318150933.png|490]]

Vícerozměrné pole:
(mega stinky fujky {} - [])
![[Pasted image 20260318151100.png|468]]

zkracování switch zápisů:
![[Pasted image 20260318152930.png|355]]

## 25.03.2026
![[Pasted image 20260325143853.png|636]]
- netřidí výsledky ani nic, prostě jak databáze xd
- .put .containsKey ...
![[Pasted image 20260325144555.png|621]]
#### Iterátory, pro odstraňování z kolekcí
![[Pasted image 20260325145152.png|529]]
![[Pasted image 20260325145652.png|506]]
![[Pasted image 20260325151449.png|530]]
![[Pasted image 20260325151520.png|521]]

s
## 01.04.2026
bruh

## 15.04.2026
[prezentace](file:///Users/boris/VS%CC%8CE/programova%CC%81ni%CC%81/Pr%CC%8Cedna%CC%81s%CC%8Cka%208.pdf)
![[Pasted image 20260415151336.png]]
![[Pasted image 20260415152607.png|637]]
- **fckng důvod proč mi mizely věci ze souboru >:C**

#### Kódování v souborech:
- Standardně se předpokládá kódování operačního systému (Windows je mrdka)
- Kódování je možné upravit pomocí
	1) InputStreamReader
	2) OutputStreamWriter
	- ![[Pasted image 20260415152834.png]]
	- ![[Pasted image 20260415153122.png]]
		- Bacha na formátování je tam prý chyba?

## 06.05.2026

