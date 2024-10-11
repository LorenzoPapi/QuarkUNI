### Esercizio 1
> *Verificare che l'applicazione $f: \mathbb{R}\to \mathbb{R}$, $x\to \frac{2x+1}{3}$ è biiettiva e trovarne l'inversa*.

Dimostriamo prima che è iniettiva: dati $x,y \in \mathbb{R}, x \neq y$ vale che:
$$
2x \neq 2y \implies 2x + 1 \neq 2y + 1 \implies \frac{2x + 1}{3} \neq \frac{2y + 1}{3} \implies f(x) \neq f(y)
$$
Per dimostrare la suriettività si imposta l'equazione $\frac{2x+1}{3} = y$ e si risolve in funzione di $x$:
$$
2x+1=3y\implies 2x=3y-1\implies x=\frac{3y-1}{2}
$$
Poiché $y \in \mathbb{R}$, la funzione è suriettiva e questa è la sua inversa.
### Esercizio 2
> *Dare esempi di applicazioni $\mathbb{R}\to\mathbb{R}$ suriettive ma non iniettive, iniettive ma non suriettive, né suriettive né iniettive*.

Nel primo caso, basta prendere $f(x) = x^3-x$ o qualunque polinomio di grado dispari con almeno 2 radici reali.
Nel secondo caso, basta prendere $f(x) = a^x, a \in \mathbb{R}^+$.
Nel terzo caso, basta prendere $\cos(x), \sin(x)$.
### Esercizio 3
> *Trovare una corrispondenza biunivoca tra l'insieme $P \subset \mathbb{N}$ dei numeri pari e l'insieme $D \subset \mathbb{N}$ dei numeri dispari. Esiste una corrispondenza biunivoca tra gli insiemi $P$ ed $\mathbb{N}$?*

Sia $f: P \to D$, $f(p) = p + 1$. È ben definita in quanto il successivo di ogni pari è dispari. È iniettiva in quanto i successori di due numeri naturali diversi sono diversi fra loro. È suriettiva in quanto ad ogni pari associo il suo successivo, quindi considero tutti i numeri dispari. È dunque biunivoca.

La funzione $f: N \to P, f(n) = 2n$ è biunivoca in quanto suriettiva e iniettiva.
### Esercizio 4
> *Dimostrare le proprietà della composizione di funzioni.*

1) $((h \circ g) \circ f)(a)= (h \circ g)(f(a)) = h(g(f(a))) = h(g \circ f)(a) = (h \circ (g \circ f)(a)$
2) Per ipotesi, $\forall a_{1},a_{2}\in A:a_{1}\neq a_{2}\implies f(a_{1})\neq f(a_{2})$ e $\forall b_{1},b_{2}\in B:b_{1}\neq b_{2}\implies g(b_{1})\neq f(b_{2})$. Ora, ponendo $b_1 = f(a_1), b_2=f(a_2)$, per ipotesi so che $b_1 \neq b_2$, quindi risulta che: $a_{1}\neq a_{2}\implies g(f(a_{1}))\neq g(f(a_{2})) \implies g \circ f$ iniettiva.
3) Per ipotesi, $\forall b \in B: \exists a \in A : f(a) = b$ e $\forall c \in C: \exists b \in B : g(b) = c$. Ora prendendo $b = f(a)$, si ottiene che $\forall c \in C : \exists a \in A : g(f(a)) = c \implies g\circ f$ suriettiva.
4) Poiché le prime due funzione sono suriettive, la composizione lo è a sua volta, idem per l'iniettività, dunque è automaticamente biiettiva.
5) Per ipotesi, $\forall a_{1},a_{2} \in A:a_{1}\neq a_{2}\implies g(f(a_{1}))\neq g(f(a_{2}))$. La contronominale equivale a $g(f(a_1)) = g(f(a_2)) \implies a_1 = a_2$: considerando quindi $f(a_1) = f(a_2) \implies g(f(a_{1})) = g(f(a_{2})) \implies a_{1} = a_{2}$ e quindi $f$ iniettiva.
6) Per ipotesi, $\forall c \in C: \exists a \in A : g(f(a)) = c$. Supponendo che $g$ non sia suriettiva, allora $\exists c \in C: \forall b \in B : c \neq g(b)$, ma poiché $\forall a \in A: g(f(a)) \in C$, e poiché $b = f(a)$, allora si raggiunge ad una contraddizione, per cui $g$ suriettiva.