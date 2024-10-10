## Insiemi
> *Siano A, B, C tre insiemi. Verificare le seguenti uguaglianze*:
> 1) $[(A \cup C)\cap B]\setminus(A \cap B) = (B \cap C)\setminus A$
> 2) $(A \cup B)\setminus(B \cap C) = (A\setminus B)\cup(B\setminus C)$

$$
\begin{align*}
[(A \cup C)\cap B]\setminus(A \cap B) &= [(A\cap B)\cup(C\cap B)]\setminus(A\cap B)= \\
&= ((A\cap B)\setminus(A\cap B))\cup((C\cap B)\setminus(A\cap B)) = \\
&= \emptyset\cup((C\cap B)\setminus(A\cap B)) \\
&= (C\cap B)\setminus A
\end{align*}
$$
$$
\begin{align*}
(A \cup B)\setminus(B \cap C) &= A \setminus(B\cap C)\cup B\setminus(B\cap C) \\
&= ((A\setminus B) \cup (A \setminus C)) \cup(B\setminus C) \\ 
&= (A\setminus B) \cup(B\setminus C)
\end{align*}
$$
> *Gli studenti di un istituto sono $1200$: di questi $780$ hanno superato Geometria, $750$ hanno superato Analisi e $1000$ hanno superato Fisica. Dire minimo e massimo numero di studenti che hanno superato tutte le tre materie.*

Possiamo definire l'insieme studenti $U=A\cup B\cup C$ dove:
- $A$ è l'insieme di quelli che hanno superato Geometria $\implies |A|=780$
- $B$ è l'insieme di quelli che hanno superato Analisi $\implies |B|=750$
- $C$ è l'insieme di quelli che hanno superato Fisica $\implies |C|=1000$
L'esercizio chiede di trovare $x=|A\cap B\cap C|$. Dal principio di inclusione esclusione, vale che
$|A\cup B\cup C| = |A|+|B|+|C| - (|A\cap B| + |A\cap C|+|B\cap C|) + x$. Dal testo, $|A\cup B\cup C|\leq 1200$. Per trovare il minimo di $x$, tutte le intersezioni devono essere minime, da cui $1330 + x \leq 1200 \implies x\geq 80\implies x=80$. Il massimo invece è $750$, altrimenti un'altra persona avrebbe passato Analisi.

> *Siano $A=\mathbb{R},B=\mathbb{Q}$. Trovare un elemento in $B\times A \setminus A \times B$ ed uno in $A\times B \setminus B \times A$*.

Poiché $A=\mathbb{Q}\cup\mathbb{I}=B\cup\mathbb{I}$ dove $\mathbb{I}$ sono gli irrazionali, si ha che:
$$
B\times A=B\times(B\cup\mathbb{I})=(B\times B)\cup(B\times \mathbb{I})
$$
$$
A\times B=(B\cup\mathbb{I})\times B=(B\times B)\cup(\mathbb{I}\times B)
$$
$$
B\times A\setminus A\times B= (B\times \mathbb{I}) \cup (\mathbb{I}\times B)
$$
$$
A\times B\setminus B\times A= (\mathbb{I} \times B) \cup (B\times \mathbb{I})
$$
dunque $(3,\sqrt{ 2 })$ è elemento del primo insieme, mentre $(\sqrt{ 2 },3)$ del secondo.
## Applicazioni
> *Determinare se $f(x)=\frac{2x+1}{x^2-2}$ è un'applicazione nei seguenti casi*

1) $f: \mathbb{N}\to\mathbb{Z}$ non è applicazione perché per $f(2)=\frac{5}{2}\notin\mathbb{Z}$;
2) $f: \mathbb{Z}\to\mathbb{Q}$ è applicazione perché divisione di interi è sempre razionale;
3) $f: \mathbb{Q}\to\mathbb{Q}$ è applicazione perché divisione di razionali è sempre razionale;
4) $f: \mathbb{R}\setminus\{\pm \sqrt{ 2 }\}\to\mathbb{R}$ è applicazione perché è sempre definita;
5) $f: \mathbb{R}\to\mathbb{R}$ non è applicazione perché $f(\pm \sqrt{ 2 })$ non sono definite.

> *Sia $f:A\to B$ applicazione e siano $S_1,S_2\subseteq A$. Provare che $f(S_1\cap S_{2})\subseteq f(S_{1})\cap f(S_{2})$ e portare un esempio che $f(S_1\cap S_{2})\subsetneq f(S_{1})\cap f(S_{2})$.

$$
m \in f(S_1\cap S_2)\implies s\in{S_{1} \cap S_{2}} \implies s\in S_{1}\land s\in S_{2} \implies m \in f(S_{1})\land m\in f(S_{2}) \implies m \in f(S_{1})\cap f(S_{2})
$$
per cui $f(S_1 \cap S_2)\subseteq f(S_{1})\cap f(S_{2})$. Prendendo $A=\{1,2,3\}, B=\{a,b\}$ e costruendo $f$ tale che $f(1) = f(3) = a, f(2)=b$, considerando $S_1 = \{1,2\}, S_2=\{2,3\}$ si ha che $S_1\cap S_{2}=\{2\}$, quindi $f(S_{1}\cap S_{2}) = f(\{2\}) = \{b\}$. Prendendo invece $f(S_1)\cap f(S_{2})=\{a,b\}\cap\{a,b\} = \{a,b\}$, per cui $f(S_{1}\cap S_{2})$ è sottoinsieme proprio di $f(S_{1}\cap S_{2})$.

> *Si considerino le applicazioni $\varphi_{1}:\mathbb{Q}\to\mathbb{Q}$ definita da $\varphi_{1}(x)=x^2+3x$ e $\varphi_{2}:\mathbb{R}^-\to\mathbb{R}^+$ definita da $\varphi_{2}(x)=\sqrt{ x^2-4x }$*.

1) L'applicazione *non* è iniettiva, dato che $\phi_1(0)=\phi_1(-3)=0$, e *non* è suriettiva, in quanto $x^2+3x = y \implies x = \frac{-3\pm \sqrt{ 9+4y }}{2}$ che è valida solo se $9+4y\geq {0}$.
2) L'applicazione *è* iniettiva, dato che $\sqrt{ x^2 -4x}=\sqrt{ y^2-4y }\implies x=y$. È anche suriettiva, in quanto $y^2=x^2-4x\implies x=2\pm \sqrt{ 4+y^2 }$, e poiché $x < 0, y>0$, l'unica inversa è $x=2-\sqrt{4+y^2}$.

> *Dato $f:\mathbb{R}^*\to\mathbb{R}, f(x)=\frac{4}{x}$, calcolare $\mathrm{Im}f,f^{-1}\left( \frac{1}{4} \right),f^{-1}(0)$.*

Preso $y=\frac{4}{x}\implies x= \frac{4}{y}$ che è sempre possibile dato che $x\neq 0$, per cui l'insieme immagine è $\mathbb{R}^*$. $f^{-1}\left( \frac{1}{4} \right) = 16$ dato che $f(16)=\frac{4}{16}=\frac{1}{4}$. Non esiste la controimmagine di $0$ poiché $0\notin\mathrm{Im}f$.
## Relazioni
> *Date le seguenti relazioni stabilire se sono riflessive, simmetriche o transitive*.

1) $x\in\mathbb{R}:x\mathcal{R}y\iff xy=1$:
	1) *simmetrica*, poiché $y\mathcal{R}x\iff yx=1=xy \iff x\mathcal{R}y$;
	2) *non riflessiva*, poiché $x\mathcal{R}x\iff x^2=1$ vale solo per $x=\pm1$;
	3) *non transitiva*, poiché $x\mathcal{R}y \land y\mathcal{R}z \implies xzy^2=1$.
2) $x\in\mathbb{R}:x\mathcal{R}y\iff e^x=e^y$:
	1) *simmetrica*, poiché $y\mathcal{R}x\iff e^y=e^x\iff e^x=e^y\iff x\mathcal{R}y$;
	2) *riflessiva*, poiché $x\mathcal{R}x\iff e^x=e^x$;
	3) *transitiva*, poiché $x\mathcal{R}y \land y\mathcal{R}z \implies e^x=e^y=e^z \implies e^x=e^z\iff x\mathcal{R}z$.
3) $(x,y)\in\mathbb{R}^2:(x,y)\mathcal{R}(x',y')\iff x+2y'=x'+2y$:
	1) *simmetrica*, poiché $(x',y')\mathcal{R}(x,y)\iff x'+2y=x+2y' \iff (x,y)\mathcal{R}(x',y')$;
	2) *riflessiva*, poiché $(x,y)\mathcal{R}(x,y)\iff x+2y=x+2y$;
	3) *transitiva*, poiché $(x,y)\mathcal{R}(x',y') \land (x',y')\mathcal{R}(x'',y'') \implies x+2y'=x'+2y\land x'+2y''=x''+2y'$ e riscrivendo $x-2y=x'-2y'\land x'-2y'=x''-2y'' \implies x-2y=x''-2y''\implies x+2y''=x''+2y$.
4) $u\in\mathcal{V}_{g}:u\mathcal{R}v\iff u\parallel v$:
	1) *simmetrica*, poiché $u\parallel v\iff v\parallel u$;
	2) *riflessiva*, poiché $u\parallel u$;
	3) *transitiva*, poiché $u\parallel v\land v\parallel z\implies u\parallel z$.

> *Sia $f:A\to B$ un'applicazione, sulla quale si pone la $a\mathcal{R}a'\iff f(a)=f(a')$, provare che è un'equivalenza, trovare una classe di equivalenza e determinare l'insieme quoziente di A.*

Tutte le relazioni sono *equivalenze* in quanto risultano in *uguaglianza di immagini*.
1) $f_1:\mathbb{R}\to\mathbb{R}, f_{1}(x)=\text{int}(x)$:
	- $\overline{1}=[1,2),\overline{2}=[2,3)$
	- l'insieme quoziente di $\mathbb{R}/\mathcal{R}=\mathbb{Z}$.
2) $f_2:\mathbb{R}^2\to\mathbb{R}, f_{2}(x,y)=y$:
	- $\overline{(1,\sqrt{ 3 })}=\{(x,\sqrt{ 3 }),x\in\mathbb{R}\}$
	- l'insieme quoziente di $\mathbb{R}^2/\mathcal{R}=\mathbb{R}$
3) $f_3:\mathbb{R}^3\to\mathbb{R}^2, f_{3}(x,y,z)=(x-y, y-z)$: 
	- detti $h=x-y,k=y-z$, fissato $x$ si ha $\overline{(1,2,3)}=\{(1+a,2+a,3+a),a\in\mathbb{R}\}$
	- 
4) $f_4:\mathbb{R}^2\to\mathbb{R}, f_{4}(x,y)=e^{x+y}$: 
	- $\overline{(1,\sqrt{ 3 })}=\{(x,y):x+y=1+\sqrt{ 3 }\}$
	- 
5) $f_5:\mathbb{R}\to\mathbb{R}^2, f_{5}(x)=(x,x)$: 

## Strutture algebriche
> *Dire se l'operazione su $\mathbb{N}$ definita da $a\star b=a^b$ è commutativa o associativa*.

Se fosse commutativa, varrebbe che $a^b=b^a$, ma prendendo $a=2,b=3$, questo non vale. Se fosse associativa si avrebbe $(a \star b) \star c = (a^b)^c = a\star(b\star c)=a\star(b^c)=a^{(b^c)}$, ma ponendo $a=b=2, c=3$ si ottiene $(2^2)^3=64=2^{2^3}=256$.

> *Verificare che $(\mathbb{Z}_{11},+,\cdot)$ è un campo.*

Sappiamo che $(\mathbb{Z}_{11},+)$ è un gruppo abeliano, in quanto l'addizione è associativa e commutativa, poi esiste l'elemento neutro ($0$) e ogni elemento ha il suo inverso (*opposto*). Inoltre, $(\mathbb{Z_{11}},+,\cdot)$ è un anello commutativo unitario, in quanto la moltiplicazione è associativa, distributiva rispetto all'addizione e commutativa, poi esiste l'elemento neutro (1). Infine è un campo in quanto il modulo $n=11$ è primo, quindi ogni elemento ha il suo inverso dato che per l'identità di Bezout è sempre possibile trovare $x=a^{-1}$ tale che $ax+11y=1$.

> *Sia $\mathcal{A}=\{f:\mathbb{R}\to\mathbb{R}|f\text{ derivabile}\}$, definendo l'operazione $\forall f,g \in \mathcal{A}\quad f+g:\mathbb{R}\to\mathbb{R}$ è l'applicazione definita da $(f+g)(x)=f(x)+g(x) \in \mathbb{R}\quad \forall x \in \mathbb{R}$. Verificare che $(\mathcal{A, +})$ è un gruppo abeliano*.

Affinché sia un gruppo abeliano:
- l'operazione deve essere chiusa in $\mathcal{A}$: somma di funzioni derivabili è derivabile;
- $+$ associativa: $((f+g)+h)(x)=(f+g)(x)+h(x) = f(x)+g(x)+h(x) = f(x) + (g(x)+h(x)) = (f+(g+h)(x)$;
- deve esistere l'elemento neutro, che è $e(x)=0$: infatti, $(f+e)(x)=f(x)+e(x)=f(x)$;
- ogni elemento deve essere invertibile: $f(x)+g(x)=0\implies g(x)=-f(x)$;
- $+$ commutativa: $(f+g)(x)=f(x)+g(x)=g(x)+f(x)=(g+f)(x)$.

> *Detto $\mathcal{A}={f:\mathbb{R}\to\mathbb{R}}$ e definita l'operazione $\forall f,g\in\mathcal{A}\quad f+g:\mathbb{R}\to\mathbb{R}$ come $(f+g)(x)=f(x)+g(x)\in\mathbb{R}\quad\forall x\in\mathbb{R}$, dire quali insiemi $\mathcal{A}_{j}$ con quest'operazione formino un gruppo*.

1) $A_{0}=\{f\in\mathcal{A}:f(1)=0\}$:
	1) $+$ è associativa;
	2) l'elemento neutro è $f(x)=0$;
	3) l'elemento inverso è $-f(x)$.
2) $A_{1}=\{f\in\mathcal{A}:f(1)=1\}$:
	1) $+$ è associativa;
	2) l'elemento neutro non esiste, perché non posso avere una funzione nulla ovunque.
3) $A_{2}=\{f\in\mathcal{A}:f(1)=f(2)=0\}$:
	1) $+$ è associativa;
	2) l'elemento neutro è $f(x)=0$;
	3) l'elemento inverso è $-f(x)$.
4) $A_{3}=\{f\in\mathcal{A}:f(x)\leq 3\ \forall x\in \mathbb{R}\}$:
	1) $+$ è associativa;
	2) l'elemento neutro è $f(x)=0$;
	3) non tutti gli elementi sono invertibili, in quanto data la funzione $f(x)=-4$ non esiste una funzione che restituisca l'elemento neutro. 
5) $A_{4}=\{f\in\mathcal{A}:\exists k \in \mathbb{R}:f(x)\leq k\ \forall x\in \mathbb{R}\}$:
	1) $+$ è associativa;
	2) l'elemento neutro è $f(x)=0$;
	3) non tutti gli elementi sono invertibili, in quanto data la funzione $f(x)=-k+1$ non esiste una funzione che restituisca l'elemento neutro. 

> *Sia $H=\{\lambda \pi|\forall\lambda\in\mathbb{Z}\}$; provare che $(H,+)$ è un gruppo abeliano.*

È l'insieme dei multipli di $\pi$. L'operazione di somma è sicuramente associativa e commutativa, inoltre esiste l'elemento neutro $0$ ottenuto con $\lambda=0$, ed essendo in $\mathbb{Z}$ esiste l'opposto di $\lambda$, per cui si ha $\lambda\pi + (-\lambda\pi)=0$.
## Insiemi numerici
> *Trovare in $\mathbb{C}$ le radici ottave di -1.*

Bisogna risolvere l'equazione $x^8 + 1=0$. Scrivendo $-1$ in forma goniometrica si ottiene $\rho=1,\vartheta=\pi \implies x_{k}=\cos\left( \frac{2\pi k+\pi}{8} \right) + i\sin\left( \frac{2\pi k+\pi}{8} \right), k=0,1,\dots,7$.

> *Risolvere in $\mathbb{C}$ l'equazione $2x^6+i=\sqrt{ 3 }$.*

Si può riscrivere $x^6-\frac{\sqrt{ 3 }-i}{2}=0$. Per scrivere il termine noto in forma complessa bisogna trovare $\rho$ e $\vartheta$ in maniera tale che:
$$
\begin{cases}
\rho \cos \vartheta =\frac{\sqrt{ 3 }}{2}\\
\rho\sin\vartheta=-\frac{1}{2}
\end{cases}
\implies
\tan \vartheta=-\frac{\sqrt{ 3 }}{3} \implies \vartheta=\frac{5\pi}{6},\rho=1
$$
Risulta quindi che $x_k=\cos\left( \frac{12k\pi+5}{36} \right)+i\left( \frac{12k\pi+5}{36} \right),k=0,1,\dots,5$

> *Trovare in $\mathbb{C}$ le radici quinte di $z=\cos\frac{5}{12}\pi+i\sin\frac{5}{12}\pi$*

Equivale a risolvere l'equazione $x^5 = z$, per cui le soluzioni sono $x_k=\cos\left(\frac {2k\pi+\frac{5}{12}\pi}{5} \right)+ i\sin\left(\frac{2k\pi+\frac{5}{12}\pi}{5}\right)=\cos\left( \frac{24k+5}{60}\pi\right)+i\sin\left( \frac{24k+5}{60}\pi\right),k=0,1,\dots,4$

> *Trovare in $\mathbb{C}$ le radici quinte di $\frac{2i+1}{i-2}$*.

Significa risolvere $x^5 = \frac{2i+1}{i-2}=\frac{(2i+1)(i+2)}{(i-2)(i+2)}=\frac{-2+2+5i}{-1-4}=\frac{5i}{-5}=-i\implies \rho=1,\vartheta=\frac{3}{2}\pi$. Quindi le radici quinte sono $x_k=\cos\left( \frac{\frac{3}{2}\pi+2k\pi}{5} \right)+i\sin\left( \frac{\frac{3}{2}\pi+2k\pi}{5} \right)=\cos\left( \frac{3+4k}{10}\pi \right)+i\sin\left( \frac{3+4k}{10}\pi \right)$.
## Polinomi
> *Sia $G=\{f(x)\in\mathbb{R}[x]:f'(0)=0\}$. Provare che le operazioni tra polinomi $+,\cdot$ sono operazioni in $G$ e verificare che $(G,+)$ è gruppo abeliano, ma $(G\setminus\{0\},\cdot)$ non lo è.*

Detto $f(x)=\sum_{k=0}^n a_{k}x^k$, la sua derivata è un polinomio $f'(x)=\sum_{k=0}^{n-1}b_{k}x^k$ con $b_i=a_{i+1}{i+1}$. Poiché $f'(0)=0\implies b_{0}=0\implies a_{1}=0$. Poiché in ogni polinomio manca il termine di primo grado, date le regole di somma è prodotto non si può ottenere questo tipo di termine a partire dagli altri, quindi le operazioni tra polinomi rimangono operazioni in $G$, ereditandone le caratteristiche principali (associatività, commutatività, distributività). Esiste l'elemento neutro che è $f(x)=0$ e ogni polinomio possiede il suo opposto che si ottiene facendo l'opposto dei coefficienti, quindi $(G,+)$ è gruppo abeliano. Invece, $(G\setminus\{0\},\cdot)$ non lo è dato che manca l'opposto: non per tutti i polinomi ne esiste un inverso tale che il loro prodotto sia $1$.

> *Determinare $a,b\in\mathbb{R}$ in modo che il polinomio $x^3-3x^2+ax+b$ abbia $2$ come radice di molteplicità $2$.*

Dal testo si comprende che il polinomio è divisibile per $(x-2)^2$. Quindi si potrebbe scrivere $x^3-3x^2+ax+b=(x-2)^2(x-\lambda) =(x^2-4x+4)(x-\lambda)=x^3-(\lambda+4)x^2+4(1+\lambda)x-4\lambda$ e per il principio di identità dei polinomi, vale che $\lambda+4=3\implies \lambda=-1$, da cui $a=0,b=4$.

> *Risolvere in $\mathbb{C}$ l'equazione $3x^4-5x^3-7x^2+15x-6=0$.*

Provando a inserire dei valori, $x=1$ risulta soluzione, quindi il polinomio è divisibile per $(x-1)$. Calcolando la divisione con Ruffini si ottiene che $(x-1)(3x^3-2x^2-9x+6)$, ma il secondo fattore si può scrivere come $x^2(3x-2)-3(3x-2)=(x^2-3)(3x-2)$, per cui le soluzioni totali sono $\left\{ -\sqrt{ 3 }, \frac{2}{3}, 1, \sqrt{ 3 } \right\}$.

> *Risolvere in $\mathbb{C}$ l'equazione $x^4-6x^3+7x^2-10x+2=0$, sapendo che ammette $1-i$ come radice.*

Ese buggato perché $1-i$ non è soluzione kek

> *Sia $x^3+ax^2+bx+c=0$ con $a,b,c\in\mathbb{C}$ di radici $\alpha_{1},\alpha_{2},\alpha_{3}$, allora valgono le formule di Vieta. Verificarlo con l'equazione $x^3-2x^2+x-2=0$.*

Si verifica che $x=2$ è soluzione, quindi si scompone con $x^2(x-2)+(x-2)=(x-2)(x^2+1)$ che ha radici $\{2,i,-i\}$. Ponendo che $a=-2, b=1, c=-2$, si ha che:
$$
\begin{cases}
\alpha_{1}+\alpha_{2}+\alpha_{3}=2+i-i=2=-a \\
\alpha_{1}\alpha_{2}+\alpha_{2}\alpha_{3}+\alpha_{3}\alpha_{1}=2i+1-2i=1=b \\ 
\alpha_{1}\alpha_{2}\alpha_{3}=2\cdot i\cdot(-i) = 2 = -c \\
\end{cases}
$$
> *Esiste un polinomio reale di grado 4 che ammette la radice $1+i$ doppia e la radice $-1$ semplice? E di grado 5?*

Di grado 4 non può esistere, dato che avere doppia radice $1+i$ implica che sia radice doppia anche $1-i$ e per il teorema fondamentale ha solo 4 radici. Invece, di 5 grado può esistere ed è $p(x)=(x-1-i)^2(x-1+i)^2(x+1)=x^5-3x^4+4x^3-4x+4$.

> *Fattorizzare in $\mathbb{R}[x]$ ed in $\mathbb{C}[x]$ il polinomio $x^4-2x^3+4x^2-6x+3$.*

Si verifica che $x=1$ è soluzione e si ottiene $(x-1)(x^3-x^2+3x-3)=(x-1)^2(x^2+3)$. Nei reali non si può procedere oltre, ma nei complessi si ottiene $(x-1)^2(x-\sqrt{ 3 }i)(x+\sqrt{ 3 }i)$.

