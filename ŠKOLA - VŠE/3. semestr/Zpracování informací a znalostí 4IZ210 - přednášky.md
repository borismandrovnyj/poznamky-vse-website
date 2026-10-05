## 21.09.2026
xgboost
[Claude](https://en.wikipedia.org/wiki/Claude_Shannon)
[prezentace č.1](file:///Users/boris/VS%CC%8CE/aZpracova%CC%81ni%CC%81%20informaci%CC%81%20a%20znalosti%CC%81/prezentace/lecture_dt_I_cz.pptx)
- log2( 0 ) je 0 definováno v tomto prostředí
![[Pasted image 20260921151703.png|439]]
- entropie = míra neuspořádanosti
	- po zjištění informace třeba že prší tak se mi chce jít míň na tennis o kolik? = informační zisk
informační zisk
![[Pasted image 20260921151935.png]]
|Sv| - počet prvku (je to množina)

![[Pasted image 20260921152647.png|403]]

- když mi třeba chybí informace tak se můlžu podívat na častý index
- prší? bohužel nefunguje sensor, tak es podívuám že když prší tak je často windy i bez znalosti dané informace v tnehle moment
![[Pasted image 20260921153722.png]]

občas vzniká problém špatné logiky viz.:
![[Pasted image 20260921154215.png]]
tady třeba každé pondělí nehrajeme, ale třeba to tak bylo náhodou a ono si to může myslet že pondělí je day off

---
![[Pasted image 20260921154528.png|490]]

---
![[Pasted image 20260921154634.png|510]]
![[Pasted image 20260921154655.png|506]]

---
![[Pasted image 20260921154944.png]]
- bobot bude hledat rozdíly a třeba nic nenajde nebo bude strom moc veliký, také se může stát že strom najde nějaký rozdíl a tak se začne rozhodvat nějak divně podle něčeho co nechceme - třeba vyřešíme dalším rozhodovacím momentem třeba míra toho jak se mi chce
---
## 05.10.2026
https://mlu-explain.github.io/
