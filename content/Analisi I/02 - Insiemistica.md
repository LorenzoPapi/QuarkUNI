Un **insieme $X$** è un oggetto per il quale la scrittura $x \in X$ è una [[01  - Logica proposizionale|proposizione]] (nozione di **appartenenza**) per tutti gli $x$ e si può descrivere per **caratteristica** (*intensiva*) o **elencazione** (*estensiva*). Si definisce **insieme vuoto** ($\emptyset$) quell'insieme per il quale $x \in \emptyset \equiv F$.

Sono definite le seguenti operazioni su due insiemi $A$ e $B$:
- **Unione**: $A \cup B = \{ x: x \in A  \lor x \in B \}$, commutativa, associativa, distributiva.
- **Intersezione**: $A \cap B = \{ x: x \in A  \land x \in B \}$, commutativa, associativa, distributiva. Se $A \cap B = \emptyset$, allora gli insiemi si dicono **disgiunti.
- **Differenza**: $A \setminus B = \{ x:x\in A \land x \notin B \}$, anti-commutativa, segue le leggi di *de Morgan*.
- **Prodotto cartesiano**: $A \times B = \{ (a,b):a\in A,b\in B \}$, distributiva.

Le relazioni tra due insiemi possono essere di:
- **Inclusione**: $A \subseteq B \equiv (x \in A \implies x \in B)$.
- **Equivalenza**: $A = B \equiv (A \subseteq  B \land B \subseteq  A$), oppure $A \times B = B \times A$.
## Insiemi numerici
$$
\mathbb{N} = \{ 0, 1, 2, 3, \dots \} \\
$$
$$
\mathbb{Z} = \{ 0, \pm1, \pm2, \pm3, \dots \}
$$
$$
\mathbb{Q} = \left\{ \frac{m}{n}: m,n\in \mathbb{Z}, n\neq 0\right\}
$$
#Todo definizione di R
$$
\mathbb{N} \subseteq \mathbb{Z} \subseteq \mathbb{Q} \subseteq \mathbb{R}
$$
## Logica predicativa
Sia $X$ un insieme. $P$ è **predicato** se $P(x)$ è una proposizione per tutti gli $x$. Valgono le medesime regole della logica proposizionale, ovvero si possono utilizzare i [[01  - Logica proposizionale#Connettivi logici|connettivi logici]] per costruire altri predicati. Un predicato può diventare una proposizione se viene **quantificato**, cioè se si dice qualcosa sull'insieme di verità del predicato stesso. Vi sono due modi principali:
- **quantificatore esistenziale**: $\exists x : P(x) \equiv P \neq \emptyset$.
	- Un suo sottotipo è il **quantificatore unico** che equivale a dire $\exists!x : P(x) \equiv |P| = 1$.
- **quantificatore universale**: $\forall x : P(x) \equiv P = X$.

La negazione **anti-commuta** i quantificatori, poiché:
1) $\lnot (\exists x : P(x))\equiv \forall x: \lnot P(x) \equiv P = \emptyset$
2) $\lnot (\forall x : P(x))\equiv \exists x :\lnot P(x) \equiv P \neq X$

