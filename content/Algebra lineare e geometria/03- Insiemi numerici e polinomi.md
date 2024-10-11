# Insiemi numerici
## $\mathbb{N}$
Il primo insieme numerico che si incontra è $\mathbb{N}$ sul quale si postula il ***principio di induzione***:
$$
A \subseteq \mathbb{N}:(0\in A\land (n\in A\implies n+1\in A))\implies A \equiv N
$$
che permette la formulazione di **dimostrazioni per induzione**, basate sul dimostrare la validità di una proposizione per un caso base e poi per un caso generico assumendo la validità del caso precedente.
## $\mathbb{Z}$
Tuttavia, si nota subito che $(\mathbb{N},+)$ **non è un gruppo**. Nasce quindi $\mathbb{Z}$ per colmare la mancanza dell'opposto, con $\mathbb{N}\subset\mathbb{Z}$, avendo ora il vantaggio che $(\mathbb{Z},+)$ è un **gruppo abeliano** nel quale equazioni del tipo $x+n=0$ hanno soluzione.
## $\mathbb{Q}$
Eppure non basta, dato che le equazioni del tipo $ax=b$ con $MCD(a,b)=1$ non hanno soluzione, dato che $(\mathbb{Z},+,\cdot)$ **non è un campo**. Si costruisce quindi $\mathbb{Q}$ per colmare la mancanza dell'inverso moltiplicativo, con $\mathbb{Z}\subset\mathbb{Q}$ che forma il **campo $(\mathbb{Q},+,\cdot)$**.
## $\mathbb{R}$
Ma nemmeno questo basta, dato che equazioni di grado superiore come $x^2 - 2 = 0$ non hanno soluzione in $\mathbb{Q}$. Si costruiscono allora i reali $\mathbb{R}$, nei quali tuttavia vi sono ancora equazioni come $x^2+1=0$. Allora è necessario costruire un campo più ampio nel quale *ogni equazione algebrica ha soluzioni*: questo è il campo dei **numeri complessi $\mathbb{C}$** che di conseguenza si dice ***algebricamente chiuso***. In questo campo vale il <u><span title='Ogni equazione algebrica a coefficienti complessi ha almeno una soluzione nel campo dei numeri complessi.'><b><i>teorema fondamentale dell'algebra</i></b></span></u>.
## $\mathbb{C}$
Sia $\mathbb{C}=\mathbb{R}\times\mathbb{R}$ e definiamo su di esso le operazioni:
- $(a,b)+(c,d)=(a+c,b+d)$
- $(a,b)\cdot(c,d)=(ac-bd,ad+bc)$
Bisogna ora verificare che $(\mathbb{C},+,\cdot)$ sia un campo:
1) $[(a,b) + (c,d)] + (e,f) = (a+c+e,b+d+f)=(a,b)+[(c,d)+(e,f)]$, quindi $+$ è associativa;
2) $(a,b) + (0,0) = (a+0,b+0)=(a,b)$, quindi $(0,0)$ è neutro di $+$;
3) $(a,b)+(c,d)=(0,0)\implies a+c=0\land b+d=0\implies c=-a\land d=-b\implies(-a,-b)$ è l'inverso di $(a,b)$;
4) $(a,b)+(c,d)=(a+c,b+d)=(c+a,d+b)=(c,d)+(a,b)$, quindi $+$ è commutativa.
Risulta quindi che $(\mathbb{C}, +)$ è un *gruppo abeliano*. Continuiamo:
1) $\begin{aligned} \left[(a,b)\cdot(c,d)\right]\cdot(e,f) &=(ac-bd,ad+bc)\cdot(e,f)\\ &=(ace-bde-adf-bcf,acf-bdf+ade+bce)\\&=(a(ce-df)-b(cf+de),a(cf+de)+b(ce-df)) \\&=(a,b)\cdot(ce-df,cf+de)\\&=(a,b)\cdot[(c,d)\cdot(e,f)]\\ &\text{quindi è associativa;} \end{aligned}$
2) $\begin{aligned} (a,b)\cdot((c,d)+(e,f)) &= (a,b)\cdot(c+e,d+f)\\ &= (ac+ae-bd-bf,ad+af+bc+be)\\ &= ((ac-bd) + (ae-bf),(ad+bc)+(ad+be))\\ &= [(a,b)\cdot(c,d)]+[(a,b)\cdot(e,f)]\\ &\text{quindi è distributiva rispetto a +;} \end{aligned}$
3) $(a,b)\cdot(c,d)=(ac-bd,ad+bc)=(ca-db,da+cb)=(c,d)\cdot(a,b)$ quindi è commutativa;
4) $(a,b)\cdot(1,0)=(a,b)$, quindi $(1,0)$ è neutro di $\cdot$;
Risulta quindi che $(\mathbb{C},+,\cdot)$ è un *anello commutativo unitario*. Infine, supponendo $(a,b)\neq(0,0)$, verifichiamo se esiste il suo inverso, ovvero la coppia $(a',b'):(a,b)\cdot(a',b')=(1,0)$. Espandendo:
$$
(aa'-bb',ab'+a'b) =(1,0)\implies \begin{equation}
\begin{cases}
aa'-bb'=1 \\
ab'+a'b=0
\end{cases}
\implies
\begin{cases}
-a^2b'-b^2b'=b \\
a'=-a\frac{b'}{b}
\end{cases}
\implies
\begin{cases}
b'=-\frac{b}{a^2+b^2} \\
a'=\frac{a}{a^2+b^2}
\end{cases}
\end{equation}
$$
che ha sempre significato, dato che $(a,b)\neq(0,0)\implies a^2+b^2\neq0$, per cui ogni elemento $(a,b)$ ha inverso $\left(\frac{a}{a^2+b^2},-\frac{b}{a^2+b^2}\right)$. Quindi $(\mathbb{C},+,\cdot)$ è un *campo*.
### Forma algebrica
Ora, si verifica che i numeri $(a,0)$ sono i numeri reali: infatti $(a,0)+(b,0)=(a+b,0)$ e $(a,0)\cdot(b,0)=(ab,0)$, quindi $\mathbb{R}\subset\mathbb{C}$, in particolare è *sottocampo*. Inoltre, il numero complesso $(0,1)$ ha la proprietà che:
$$
(0,1)\cdot(0,1)=(0-1,0+0)=(-1,0)
$$
ovvero il suo quadrato è il numero reale $-1$. Infine, ogni numero si può scrivere in forma unica come:
$$
(a,b)=(a,0)+(0,1)\cdot(b,0)=(a,0)+(0,b)=(a,b)
$$
per cui, chiamando i complessi che si rivelano numeri reali $(a,0)=a$ e $(0,1)=i$ si ottiene che:
$$
\forall z \in \mathbb{C}:\exists a,b \in\mathbb{R}:z=a+ib, i^2=-1
$$
$a$ si chiama ***parte reale***, mentre $b$ ***parte immaginaria***. Se $z=a+ib$, allora $\overline{z}=a-ib$ si chiama ***coniugato di $z$***. Detti $z=a+bi,w=c+di\in\mathbb{C}$, si ha che:
1) $\overline{(\overline{z})}=\overline{(a-bi)} = a+bi=z$
2) $z+\overline{z}=a+bi+a-bi=2a\in\mathbb{R}$
3) $z\cdot \overline{z}=(a+bi)(a-bi)=a^2+b^2\in\mathbb{R}$
4) $\overline{z+w}=\overline{(a+c) + i(b+d)}=(a+c)-i(b+d)=(a-ib)+(c-id)=\overline{z}+\overline{w}$
5) $\overline{z\cdot w}=\overline{(ac-bd)+i(ad+bc)}=(ac-bd)-i(ad+bc)=(a-ib)(c-id)=\overline{z}\cdot\overline{w}$
6) $|z|=\sqrt{ z\cdot \overline{z}}=\sqrt{ a^2+b^2 }$ si chiama ***modulo di $z$*** e gode delle stesse proprietà del *valore assoluto*.
### Forma trigonometrica
Un numero complesso $a+ib$ individua in un piano a coordinate cartesiane ortogonali un punto $P\equiv(a,b)\equiv a+ib$. Definendo:
- $\rho=\overline{OP}=|z|=\sqrt{ a^2+b^2 }$ come ***modulo***,
- $\vartheta\in[0,2\pi)$ come l'angolo di cui deve ruotare in senso antiorario l'asse $x$ per sovrapporsi equiverso ad $\overline{OP}$, detto ***anomalia***,
il numero complesso può essere scritto come
$$
a+ib=\rho(\cos\vartheta+i\sin\vartheta)
$$
Si osserva che due numeri complessi sono uguali se hanno lo stesso modulo e differiscono nelle loro anomalie di $2\pi$. Presi due numeri complessi in forma trigonometrica:
$$
\begin{align}
&\rho(\cos\vartheta+i\sin\vartheta)\cdot\rho'(\cos\vartheta'+i\sin\vartheta')=\\&=\rho\rho'(\cos\vartheta\cos\vartheta'-\sin\vartheta\sin\vartheta'+i(\cos\vartheta'\sin\vartheta+\sin\vartheta'\cos\vartheta))\\&=\rho\rho'(\cos(\vartheta+\vartheta')+i(\sin(\vartheta+\vartheta')))
\end{align}
$$
e nel caso in cui i due numeri siano uguali, generalizzando ad $n$ moltiplicazioni si ottiene la ***formula di de Moivre***:
$$
z^n=\rho^n(\cos n\vartheta+i\sin n\vartheta)\quad \forall n\in\mathbb{N}
$$
Consideriamo ora $z^{-1}=\left(\frac{a}{a^2+b^2},\frac{-b}{a^2+b^2}\right)$, ovvero l'inverso moltiplicativo di $z$. Si ha che $\rho'=\sqrt{\frac{a^2+b^2}{(a^2+b^2)^2}}=\sqrt{ \frac{1}{a^2+b^2} }=\rho^{-1}$. Dall'identità $z\cdot z^{-1}=1$ si ottiene che:
$$
\begin{cases}
\cos(\vartheta+\vartheta')=1\\
\sin(\vartheta+\vartheta')=0
\end{cases}
\implies
\vartheta+\vartheta'=0\implies\vartheta'=-\vartheta
$$
per cui $z^{-1}=\frac{1}{\rho}(\cos(-\vartheta)+i\sin(-\vartheta))=\frac{1}{\rho}(\cos\vartheta-i\sin\vartheta)$ che generalizza la formula ad esponente $m \in \mathbb{Z}$.
### Equazioni in $\mathbb{C}$
Consideriamo le equazioni $x^n-\alpha=0$, con $\alpha\in\mathbb{C}_{0}$, $n\in\mathbb{N}_{0}$. Poniamo $a=\rho(\cos\vartheta+i\sin\vartheta)$: i numeri da cercare dovranno soddisfare
$$
x^n=\sigma^n(\cos n\tau+i\sin n\tau)=\rho(\cos\vartheta+i\sin\vartheta)
$$
ma da qui segue che
$$
\begin{cases}
\sigma^n=\rho \\
n\tau-\vartheta=\lambda(2\pi),\ \lambda\in \mathbb{Z}
\end{cases}
\implies
\begin{cases}
\sigma=\sqrt[n]{\rho} \\
\tau=\frac{2\pi\lambda+\vartheta}{n}
\end{cases}
$$
per cui si ottengono soluzioni del tipo $x_{\lambda} = \sqrt[n]\rho\left( \cos\left( \frac{2\pi \lambda+\vartheta}{n}\right) + i\sin\left(\frac{2\pi \lambda+\vartheta}{n}\right)\right)$, che differiscono solo per l'anomalia. Supponiamo che per due valori $h,k$ con $0\leq h, k < n, h\neq k$ le corrispettive radici coincidessero: allora le loro fasi differirebbero di multipli di $2\pi$ per cui
$$
\frac{2\pi h+\vartheta}{n}-\frac{2\pi k+\vartheta}{n}=2\pi \frac{h-k}{n}
$$
ma per le condizioni di $h,k$, si ha che $\frac{h-k}{n}\notin\mathbb{Z}$, quindi $x_0, x_1, \dots, x_{n-1}$ sono radici distinte. In generale invece, si può scrivere $\lambda = qn + r$, con $0\leq r < n$, per cui la differenza di anomalie tra $x_r$ e $x_\lambda$ è
$$
\frac{2\pi\lambda+\vartheta}{n}-\frac{2\pi r+\vartheta}{n}=2\pi \frac{\lambda-r}{n}=2\pi \frac{qn}{n} = 2q\pi
$$
per cui $x_\lambda=x_r$ e quindi vi sono solamente $n$ radici distinte.
# Polinomi ed equazioni algebriche
Sia $(K,+,\cdot)$ un campo: si dice ***polinomio nell'indeterminata $x$ a coefficienti in $K$*** ogni espressione del tipo
$$
f(x)=a_{0}+a_{1}x+\dots+a_{n}x^n,\ a_{i}\in K
$$
L'insieme di questi polinomi nel campo $K$ si indica con $K[x]$ e ogni polinomio individua una funzione $f: K\to K$. Se $f(x) \in K[x]$ si dice ***grado di $f(x)$ il massimo degli interi $i$ per cui $a_i\neq0$***. Ovvero, $a_d\neq0\land a_i=0\ \forall i > d \iff deg(f(x))=d$. Nel caso del *polinomio nullo*, ovvero un polinomio per cui $\forall i:a_i=0$, il grado non è definito. Due polinomi scritti in forma normale sono ***identici*** se e solo se **coincidono i loro coefficienti per ogni grado**.

Si definiscono le operazioni di somma e prodotto in $K[x]$, prendendo per esempio $\displaystyle f(x)=\sum_{i=0}^n a_ix^i$ e $\displaystyle g(x)=\sum_{i=0}^m b_ix^i$, ponendo $t=\max\{m,n\}$, si ha:
- $\displaystyle f(x)+g(x)=(a_{0}+b_{0})+(a_{1}+b_{1})x+\dots+(a_{t}+b_{t})x^t=\sum_{i=0}^t(a_{i}+b_{i})x^i$;
- $\displaystyle f(x)\cdot g(x) = a_{0}b_{0} + (a_{0}b_{1} + a_{1}b_{0})x+\dots=\sum_{i=0}^{m+n}c_{i}x^i$, con $\displaystyle c_{i}=\sum_{h=0}^{i} a_{h}b_{i-h}$.
Risulta quindi che $(K[x],+,\cdot)$ è un *anello commutativo unitario* e si ricava che:
- $deg(f(x)+g(x))\leq t = \max\{m,n\}$.
- $deg(f(x)g(x))=m+n$.
Vale la regola di **annullamento del prodotto**: gli anelli nei quali vale questa proprietà si chiamano ***domini d'integrità***.

Siano $f(x),g(x)\in K[x]$, con $g(x)\neq0$. Allora esistono due polinomi $q(x),r(x)\in K[x]$ tali che:
$$
f(x)=g(x)q(x)+r(x),\ r(x)=0 \lor deg(r(x))<deg(g(x))
$$
Vale che $deg(q(x))=deg(f(x))-deg(g(x))$.
## Equazioni algebriche
Un'equazione ***algebrica*** è un'equazione del tipo $f(x)=0, f(x)\in K[x]$. Un elemento $\alpha \in K$ si dice ***soluzione*** (*radice*) dell'equazione $f(x)=0\iff f(\alpha)=0$. Elenchiamo dei teoremi:
- ***Ruffini***: sia $f(x),g(x)\in K[x],deg(f(x))=n,deg(g(x))=n-1$ e $\alpha \in K$:
	- $f(x)=(x-\alpha)g(x)\implies f(\alpha)=(\alpha-\alpha)g(\alpha)=0$
	- $f(\alpha)=0\implies f(x)=(x-\alpha)g(x)+r$, ma $0=(\alpha-\alpha)g(\alpha)+r\implies r=0$
	dunque $f(\alpha)=0\iff f(x)=(x-\alpha)g(x)$.
- ***Fondamentale***: *ogni equazione algebrica di grado $n$ ammette al più $n$ soluzioni*:
	- $n=1$ è ovvio perché $ax-b=0\implies x=a^{-1}b$;
	- supponiamo vero per grado $< n$ e consideriamo $f(x)\in K, deg(f(x))=n$. Se $f(x)=0$ non ha soluzioni, la tesi è valida; se invece ha la soluzione $\alpha$, allora per *Ruffini* si ha che $f(x)=(x-\alpha)g(x)$, con $deg(g(x))=n-1$ che ha al più $n-1$ soluzioni, sommata alla soluzione già esistente implica che $f(x)$ ha al massimo $n$ soluzioni.
- ***Fondamentale (II)***: *ogni equazione complessa ammette $n$ soluzioni*:
	- $n=1$ è ovvio perché $\mathbb{C}$ è un campo;
	- supponendo vero per grado $<n$, poiché $f(x)$ ha almeno una soluzione $\alpha_1$, vale che $f(x)=(x-\alpha_1)g(x)$ con $deg(g(x))=n-1$, da cui segue che ha una soluzione in più di $g(x)$, che per ipotesi induttiva ne ha $n-1$, quindi ha $n$ soluzioni.
## Proprietà delle radici
- Alcune radici potrebbe essere ***molteplici***: detto $s \in \mathbb{N},f(x)\in K[x],\alpha \in K,f(\alpha)=0$ si dice *s-upla* se vale che $f(x)=(x-\alpha)^sg(x),g(\alpha)\neq {0}$. Così si può precisare meglio il teorema fondamentale affermando che ***ogni equazione complessa ammette $r$ soluzioni distinte $\alpha_{1},\alpha_{2},\dots,\alpha_{r}$ ciascuna con molteplicità $s_1,s_2,\dots,s_r$ tali che $s_{1}+s_{2}+\dots+s_{r}=n$.***
- Due equazioni si dicono ***equivalenti*** se hanno le stesse *soluzioni* e *molteplicità*. Se un'equazione ha **radici razionali** della forma $\frac{r}{s}$, allora varrà che $r|a_0, s|a_n$.
- Sia $f(x)\in\mathbb{C}[x],\alpha \in\mathbb{C}:f(\alpha)=0$ con molteplicità $m$. Allora $\overline{f}(\overline{\alpha})=0$ con molteplicità $m$. Segue che se $f(x)\in R[x]$, allora $f(\alpha)=0\implies f(\overline{\alpha})=0$ poiché $\overline{f}(x)=f(x)$. Segue anche che, se il polinomio ha grado dispari, ha almeno una soluzione reale: infatti, dal corollario precedente, se esiste una soluzione $\alpha \in \mathbb{C}\setminus\mathbb{R}$, allora $\alpha \neq\overline{\alpha}$, quindi vanno sempre in coppia, ma essendo $n$ dispari ne esiste almeno una singola, cioè per cui $\alpha=\overline{\alpha}$, quindi $\alpha$ è reale.
- Un polinomio $f(x)\in K[x]$ si dice ***irriducibile*** se $f(x)=g(x)h(x)\implies g(x)\in K \lor h(x) \in K$.
- Ogni polinomio $f(x) \in K[x]$ si può **scomporre unicamente in polinomi irriducibili** e quindi $K$ è un ***dominio a fattorizzazione unica***.
- Gli unici polinomi irriducibili in $\mathbb{C}$ hanno grado $1$, mentre in $\mathbb{R}$ vi sono anche quelli di grado $2$ con discriminante $< 0$.