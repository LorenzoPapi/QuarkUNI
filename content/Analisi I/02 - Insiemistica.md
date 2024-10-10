Un **insieme $X$** è un oggetto per il quale la scrittura $x \in X$ è una [[01  - Logica proposizionale|proposizione]] (nozione di **appartenenza**) per tutti gli $x$ e si può descrivere per **caratteristica** (*intensiva*) o **elencazione** (*estensiva*). Si definisce **insieme vuoto** ($\emptyset$) quell'insieme per il quale $x \in \emptyset \equiv F$.

Sono definite le seguenti operazioni su due insiemi $A$ e $B$:
- **Unione**: $A \cup B = \{ x: x \in A  \lor x \in B \}$, commutativa, associativa, distributiva.
- **Intersezione**: $A \cap B = \{ x: x \in A  \land x \in B \}$, commutativa, associativa, distributiva. Se $A \cap B = \emptyset$, allora gli insiemi si dicono **disgiunti.
- **Differenza**: $A \setminus B = \{ x:x\in A \land x \notin B \}$, anti-commutativa, segue le leggi di *de Morgan*.
- **Prodotto cartesiano**: $A \times B = \{ (a,b):a\in A,b\in B \}$, distributiva.

Le relazioni tra due insiemi possono essere di:
- **Inclusione**: $A \subseteq B \equiv (x \in A \implies x \in B)$.
- **Equivalenza**: $A = B \equiv (A \subseteq  B \land B \subseteq  A$), oppure $A \times B = B \times A$.
## Logica predicativa
Sia $X$ un insieme. $P$ è **predicato** se $P(x)$ è una proposizione per tutti gli $x$. Valgono le medesime regole della logica proposizionale, ovvero si possono utilizzare i [[01  - Logica proposizionale#Connettivi logici|connettivi logici]] per costruire altri predicati. Un predicato può diventare una proposizione se viene **quantificato**, cioè se si dice qualcosa sull'insieme di verità del predicato stesso. Vi sono due modi principali:
- **quantificatore esistenziale**: $\exists x : P(x) \equiv P \neq \emptyset$.
	- Un suo sottotipo è il **quantificatore unico** che equivale a dire $\exists!x : P(x) \equiv |P| = 1$.
- **quantificatore universale**: $\forall x : P(x) \equiv P = X$.

La negazione **anti-commuta** i quantificatori, poiché:
1) $\lnot (\exists x : P(x))\equiv \forall x: \lnot P(x) \equiv P = \emptyset$
2) $\lnot (\forall x : P(x))\equiv \exists x :\lnot P(x) \equiv P \neq X$
## Insiemi ordinati

> [!definition] Insieme ordinato
> Si dice ***insieme ordinato $(X,\leq)$*** ove $\leq$ è una ***[[01 - Insiemi, applicazioni, relazioni#Relazioni|relazione d'ordine]]***.
> Se $\exists x,y \in X: x \leq y \land y \geq x \equiv F$, allora si dice *parzialmente* ordinato (es: *grafi aciclici*), altrimenti è *totalmente* ordinato.

> [!definition] Maggioranti, minoranti, massimi, minimi, estremi
> Sia $A\subseteq(X, \leq)$: si definiscono:
> - $M$ ***maggiorante di A*** $\iff M \geq a\ \forall a$:
> 	- $M \in A \iff M = \max A$;
> 	- $M$ minimo $\iff$ $M = \sup A$.
>- $m$ ***minorante di A*** $\iff m \leq a\ \forall a$:
>     - $m \in A \iff m = \min A$;
>     - $m$ massimo $\iff$ $m = \inf A$.

> [!theorem ] Unicità del massimo
> *Sia $A\subseteq (X, \leq)$ e $\exists \max A=M$. Allora, $M$ è unico e $M=\sup A$*.
> 
`\begin{proof}`
Supponiamo per assurdo che esistano due massimi, $M_{1},M_{2}\in A, M_1 \neq M_2$ che possono essere ordinati da $\leq$. Per ipotesi, $M_1\geq M_{2}$ e $M_2\geq M_{1}$ e per la proprietà antisimmetrica, vale che $M_1=M_2$, assurdo. Quindi il massimo $M$ è unico.
Supponendo per assurdo che ci sia un maggiorante più piccolo di $M$, implicherebbe che $\exists M_{0}<M:M_{0}\geq a\ \forall a \in A$, ma poiché $M\in A$, si giunge ad un assurdo, quindi $\sup A =M$.`\end{proof}`

> [!theorem ] Unicità del minimo
> Sia $A\subseteq (X, \leq)$ e $\exists \min A=m$. Allora, $m$ è unico e $m=\inf A$.
> 
`\begin{proof}`
Supponiamo per assurdo che esistano due minimi, $m_{1},m_{2}\in A, m_1 \neq m_2$ che possono essere ordinati da $\leq$. Per ipotesi, $m_1\geq m_{2}$ e $m_2\geq m_{1}$ e per la proprietà antisimmetrica, vale che $m_1=m_2$, assurdo. Quindi il massimo $m$ è unico.
Supponendo per assurdo che ci sia un minorante più grande di $m$, implicherebbe che $\exists m_{0}>m:m_{0}\leq a\ \forall a \in A$, ma poiché $m\in A$, si giunge ad un assurdo, quindi $\inf A =m$.`\end{proof}`

> [!theorem] Unicità degli estremi
> Sia $A\subseteq (X, \leq)$ e $\exists \sup A$ o $\exists \inf A$. Allora essi sono unici.
> `\begin{proof}`
> Dimostriamo per il $\sup A$, per l'$\inf A$ è analogo. Considerando l'insieme di tutti i maggioranti, esso è un sottoinsieme $B\subseteq A$ nel quale vale la relazione d'ordine. Allora esiste il minimo di questo sottoinsieme che è infatti il $\sup A$ e per il teorema 02.3 è unico. `\end{proof}`

> [!definition] Limitatezza
> Sia $A\subseteq(X, \leq)$: si dice che:
>1) $A$ è ***limitato superiormente*** $\iff \exists M$ *maggiorante* per $A$.
>2) $A$ è ***limitato inferiormente*** $\iff \exists m$ *minorante* per $A$.
>3) $A$ è ***limitato*** $\iff A$ *limitato inferiormente e superiormente*.

> [!definition] Completezza
 $(X,\leq)$ è ***completo*** $\iff (\forall A\subseteq(X,\leq),A\neq\emptyset,A\text{ limitato superiormente} \implies \exists \sup A)$. Vale lo stesso considerando gli insiemi limitati inferiormente e l'esistenza dell'estremo inferiore.

> [!example]
> Tutti gli insiemi ordinati di 3 punti sono completi?

> [!theorem] 
> Se un insieme finito è **totalmente ordinato $\implies$ completo**.
> `\begin{proof}`
> Considerato un insieme finito di punti ed una relazione d'ordine che renda l'insieme ordinato, l'unica configurazione possibile per renderlo *totalmente* ordinato è quella di posizionare i punti su una retta e collegare ogni precedente col suo successivo. In ogni altra configurazione si generano almeno 2 punti sullo stesso livello ma non collegati dalla relazione, altrimenti il grafo non sarebbe aciclico. Quindi essendo totalmente ordinato esiste sempre il massimo dell'insieme e per il teorema 02.2 coincide con il massimo, per cui è completo. `\end{proof}`
### Insiemi numerici
$$
\mathbb{N} = \{ 0, 1, 2, 3, \dots \} \\
$$
$$
\mathbb{Z} = \{ 0, \pm1, \pm2, \pm3, \dots \}
$$
$$
\mathbb{Q} = \left\{ \frac{m}{n}: m,n\in \mathbb{Z}, n\neq 0\right\}
$$
$$
\mathbb{N} \subseteq \mathbb{Z} \subseteq \mathbb{Q}
$$
$\mathbb{N},\mathbb{Z}$: sono infiniti totalmente ordinati e completi.
$\mathbb{Q}$: totalmente ordinato ma non completo perché $\sqrt{2} \notin \mathbb{Q}$. Si dimostra per assurdo. Da qui risulta infatti che, preso il sottoinsieme $A=\{x\in\mathbb{Q}:0<x^2<2\}$, esso possiede almeno un maggiorante ($2$), ma $\sup A = \sqrt{ 2 }\notin\mathbb{Q}\implies \text{incompletezza}$.