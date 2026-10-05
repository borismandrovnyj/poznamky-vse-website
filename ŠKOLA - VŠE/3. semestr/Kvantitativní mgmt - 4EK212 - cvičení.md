#### Body
![[Pasted image 20260921180631.png]]

[educational licence](https://www.lindo.com/index.php/news/informs-o-r-and-analytics-student-team-competitors/research-license-for-lingo)
[download link](https://www.lindo.com/index.php/ls-downloads/try-lingo)
idk proč má macOS jenom starou verzi?!

## 24.09.2026
[jeho stránky pro výuku](https://janfabry.cz/vyuka.html)
https://janfabry.cz/4EK212-kvantitativni-management.html

![[Pasted image 20260924144608.png|494]]
- ### Ekonomický model je většinou to zadání
	- první co hledáme jsou procesy - třeba výroba (vezme vstupy -> výstupy)
	- činitelé - něco co ovlivňuje ty procesy 
		- technologie, suroviny, lidi
	- cíl (kritérium) - kyž vyrbíme x výrobků tolik vuděálam

- ### Mat
	- proměnný = procesy
	- pdomínky:
		- $x_1 + 2x_2 ≤ 500$
		- ≥
		- =
	- účelová funkce:
		- $z = 150x_1 + 200x -> max$

#### Řešení
- přípustné - vyhovuje všem omezujícím podmínkám, splňuje je všechny
	- může nebýt žádné - divný podmínky, nebo chyba formulace
- nepřípustné porušuje aspoň jednu
- optimální musí být přípustné a zároveň dává nejlepší hodnotu účelové fce
	- může jich být, ale více
		- třeba se tam dostaneme různými způsoby
	- může neexistovat - většinou chyba formulace


### Úloha výrobního plánování
![[Pasted image 20260924145439.png|717]]
- 2 procesy = 2 proměnné
- jestli to je činitel tak to má omezený množství - třeba x hodin
- 3 činitelé
	- řezbácká práce, dokončovaí práce, a dřevo

$x_1 = počet vyrobených autíček \ [ks/měsíc]$
$x_2 = -||- \ vláčků \ [ks/měsíc]$
$Zisk = Tržby - Náklady$
$T = 820x_1  + 1150x_2$
	820 a 1150 jsou jednotlivé ceny za daný produkt
$N_{dřevo} = 100x_1 + 180x_2$
	100 a 180 jsou náklady na dřevo na výrobu
$N_{řeznická \ práce} = 150⋅1x_1 + 150⋅2x_2$
$N_{dokončovací \ práce} = 120⋅1x_1 + 120⋅2x_2$
$Z = 450x_1 + 550x_2 \rightarrow \ max$

$x_1 + 2x_2 ≤ 5000$ (ŘP)
$x_1 + x_2 ≤ 3000$ (DP)
$x1 \ \ \ \ \ \ \ \ \ ≤ 2000$ (Pa)
$x_1, \ x_2 ≥ 0, \ celé$
$x_1,x_2 \ - \ celé$

zbytek v sešitě

## 01.10.2026
![[KVAM-cviceni 1.pptx]]
### Směšovací problémy
![[Pasted image 20261001143840.png|487]]

### Příklad směšovací problémy
![[Pasted image 20261001144336.png]]
4 krmiva = 4 proměnný
$x_1$ = množství krmiva K_i [v Kg] na výsledné směsi (i = 1,2,3,4)
$z= 20x_1 + 80x_2 + 60x_3 + 30x_4 \rightarrow min$

3 omezující podmínky
1. bílkoviny ≥100
	1. $3x_2 + x_3 + 2x_4 ≥ 100$
2. škrob ≥300
	1. $x_1+2x_2+3x_3 ≥ 300$
3. hmotnost ≥200
	1. $x_1+x_2+x_3+x_4 ≥ 200$ 
4. $x_i≥0$ (spíš ze začátku to nedávat, ale pokud výjde hnusné číslo tak podle reality to chci dát smysluplně)

#### Lingo řešení:
![[Pasted image 20261001145640.png|553]]

$z_0 = 6600 Kč$

$x^T = (120, 0, 60, 20)$ - vektor a je to na tou hmotnost
		0; 0; 0;) - jestliže by chtěli celej vektor i se slack/surplus (přebytkové proměnné)

redukovaný ceny (náklady)
- ta desítka to znamená že kdyby bylo levnjší o 10 $x_2$, tak by to bylo kupovatelný jinak je pro nás teď moc drahý
- další interpretace - jestliže mě někdo donutí kupovat $x_2$ tak se mi zdraží náklady o 10
	- taky levá strana celé číslo | pravá strana 0 a obráceně

$u^T = (0, 10 , 0, 0)$ - vektor redukovaných cen

stínové ceny - dual price
- pomocná tabulka - podmínka -> max/mib -> +/-

|     | ≤   | ≥   | MFC |
| --- | --- | --- | --- |
| max | +   | -   | 10  |
| min | -   | +   | 30  |
každá jendotka kolik stojí
každej kg stojí +6kč
**týká se přímo omezeni**

### Příklad optimalizace portfolia:
- více podmínek - dělá méně optimální řešení
![[Pasted image 20261001152118.png]]
![[Pasted image 20261001152435.png]]

5 proměnných
$x_i = částka \ investovaná \ do \ i-tého \ cenného \ papíru \ [v \ Kč]$
$z= 0,12x_1 + 0,09x_2 + 0,15x_3 + 0,07x_4 + 0,06x_5 \rightarrow max$

podmínky:
$x_1+x_2+x_3+x_4 = 2 \ 000 \ 000$ (budget)

$x_4 ≤ 200 \ 000$ (mlékárny)

$x_5 ≥ 400 \ 000$ (obligace)

$x_1 ≤ 800 \ 000$ (diverzifikace)
$x_2 ≤ 800 \ 000$
$x_3 ≤ 800 \ 000$

(index rizika ≤ 0,05)
$0,07⋅\frac{x_1}{2 \ mil.} + 0,09⋅\frac{x_2}{2 \ mil.} + 0,05⋅\frac{x_3}{2 \ mil.} + 0,03⋅\frac{x_4}{2 \ mil.} + 0,01⋅\frac{x_5}{2 \ mil.}≤0,05$

$x_i ≥ 0, \ i=1,2, \ ... \ ,5 \ nebo \ taky \ n$ (kladná)

#### Lingo řešení
![[Pasted image 20261001155319.png|717]]

