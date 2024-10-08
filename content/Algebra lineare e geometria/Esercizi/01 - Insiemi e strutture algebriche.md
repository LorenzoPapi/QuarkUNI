## Insiemi
> *Siano A, B, C tre insiemi. Verificare le seguenti uguaglianze*:
> 1) $[(A \cup C)\cap B]\setminus(A \cap B) = (B \cap C)\setminus A$
> 2) $(A \cup B)\setminus(B \cap C) = (A\setminus B)\cup(B\setminus C)$

$$
\begin{align}
[(A \cup C)\cap B]\setminus(A \cap B) &= [(A\cap B)\cup(C\cap B)]\setminus(A\cap B)= \\
&= ((A\cap B)\setminus(A\cap B))\cup((C\cap B)\setminus(A\cap B)) = \\
&= \emptyset\cup((C\cap B)\setminus(A\cap B)) \\
&= (C\cap B)\setminus A
\end{align}
$$
$$
\begin{align}
(A \cup B)\setminus(B \cap C) &= A \setminus(B\cap C)\cup B\setminus(B\cap C) \\
&= ((A\setminus B) \cup (A \setminus C)) \cup(B\setminus C) \\ 
&= (A\setminus B) \cup(B\setminus C)
\end{align}
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
$$B\times A=B\times(B\cup\mathbb{I})=(B\times B)\cup(B\times \mathbb{I})$$
$$A\times B=(B\cup\mathbb{I})\times B=(B\times B)\cup(\mathbb{I}\times B)$$
$$B\times A\setminus A\times B= (B\times \mathbb{I}) \cup (\mathbb{I}\times B)$$
$$A\times B\setminus B\times A= (\mathbb{I} \times B) \cup (B\times \mathbb{I})$$
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

> *Detto $\mathcal{}$*