# Operazioni
Si dice ***operazione*** (*binaria, interna*) **definita su un insieme $A$** qualunque **applicazione**:
$$
\phi:A\times A\to A;\ \phi(a,b) \equiv a \star b
$$
Si definiscono ora le possibili **pSeroprietà** delle operazioni:
- ***associatività***: $\forall a,b,c\in G: (a\star b)\star c=a\star(b\star c)$
- ***commutatività***: $\forall a,b\in G: a\star b=b\star a$
## Elemento neutro
Un elemento $e \in G$ si dice ***neutro in $(G, \star)$*** se $\forall a \in G: e\star a = a \star e = a$.

Supponendo che vi siano due elementi neutri distinti, $e_{1},e_{2}$, per ipotesi vale che $(e_{1}\star e_{2}=e_{2} \land e_{1}\star e_{2}=e_{1}) \implies e_1=e_2$ quindi si dimostra l'***unicità dell'elemento neutro***.
## Elemento inverso
Un elemento $a \in G$ si dice ***invertibile in $(G, \star)$*** se $\exists a' \in G: a\star a' = a' \star a = e$ e si indica come $-a$ o $a^{-1}$.

Supponendo che l'operazione sia associativa e che vi siano due elementi inversi, $a',a''$, per ipotesi $a\star a' = a' \star a = a'' \star a = a \star a'' = e \implies a' = a'\star e = a' \star a \star a'' = a''$ quindi si dimostra l'***unicità dell'inverso***.
## Operazioni esterne
Dati due insiemi $K, V$ si definisce ***operazione esterna di $V$ su $K$ qualunque applicazione***:
$$
f:K\times V \to V;\ a\in K, v\in V:f(a,v)=a\cdot v\in V
$$
# Strutture algebriche
## Gruppo
Detto $G$ insieme su cui è definita l'operazione $\star$, $(G,\star)$ è un ***gruppo*** se:
1) l'operazione $\star$ è **associativa**
2) esiste l'**elemento neutro $e$**
3) ogni elemento $g \in G$ è **invertibile**
In particolare, se vale anche la **commutatività** il gruppo si chiamerà ***abeliano*** (*commutativo*). Esempi sono $(\mathbb{Z}, +)$, $(R^3, +)$
## Anello
Detto $G$ insieme su cui sono definite le operazioni $+, \cdot$, $(A,+,\cdot)$ è un ***anello*** se:
1) $(A,+)$ è un **gruppo abeliano**
2) $\cdot$ è **associativa**
3) $\forall a,b,c \in A: a\cdot(b+c) = a\cdot b + a \cdot c;\ (a+b)\cdot c = a \cdot c + b \cdot c$, ovvero se $\cdot$ gode della proprietà ***distributiva*** rispetto a $+$.
In particolare, se vale anche la **commutatività di $\cdot$**, l'anello si chiamerà ***commutativo***.

Poiché ogni anello è un gruppo rispetto a $+$, esiste l'elemento neutro che si indicherà con $0$.

Consideriamo ora $z = a \cdot 0$: allora, $z = a \cdot (0 + 0) = a \cdot 0 + a \cdot 0 = z + z$, ma poiché $z \in A$, ammette un opposto e addizionandolo si ha $z + (-z) = z + z + (-z) \implies 0 = z$. Analogamente si dimostra che $0\cdot a = 0$.

Inoltre, presi $a,b\in A$, vale che $a \cdot b + (-a)\cdot b = (a - a)\cdot b = 0\cdot b = 0 \implies -(a \cdot b) =(-a)\cdot b$. Analogamente si dimostra che $-(a\cdot b) = a\cdot(-b)$.

Se esiste l'**elemento neutro rispetto a $\cdot$**, indicato con $1$ e detto **unità**, l'anello si dice ***unitario***.
## Campo
Un **anello commutativo unitario $(K,+,\cdot)$** nel quale **ogni elemento $g\neq0$ è invertibile rispetto a $\cdot$** si dice ***campo***. Esempi sono $(\mathbb{Q}, +, \cdot)$,$(\mathbb{R}, +, \cdot)$, $(\mathbb{Z}_{p}, +, \cdot)$ con $p$ primo.

Supponiamo che $a,b \in K: a\cdot b=0$. Se $a = 0$, allora non c'è altro da dire; altrimenti, se $a\neq 0$, esiste il suo opposto $a^{-1}$ e moltiplicando ambi i membri si ottiene $a^{-1}\cdot a\cdot b = a^{-1}\cdot 0 \implies b = 0$, quindi si dimostra la che ***almeno uno dei fattori è $0$***.
## Sottostrutture
Sia $(G,\star$) un gruppo e sia $S\subseteq G$: $S$ è ***sottogruppo*** di $G$ se $(S, \star)$ è un gruppo.
Sia $(A,+,\cdot$) un anello e sia $A'\subseteq A$: $A'$ è ***sottoanello*** di $A$ se $(A', +,\cdot)$ è un anello.
Sia $(K,+,\cdot$) un campo e sia $K'\subseteq K$: $K'$ è ***sottocampo*** di $K$ se $(K', +,\cdot)$ è un campo.
