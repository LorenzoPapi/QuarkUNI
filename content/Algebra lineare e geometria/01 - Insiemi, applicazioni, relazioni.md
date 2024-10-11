# [[02 - Insiemistica|Insiemi]]
# Applicazioni
> [!definition] Applicazione
Detti $A, B$ insiemi, si definisce ***applicazione*** (*funzione*) da $A$ (*dominio*) a $B$ (*codominio*) una ***legge che associa ad ogni elemento di A uno e un solo elemento di B***. Quindi: $$
f:A\to B \iff \forall a \in A: \exists!\ b \in B: b=f(a)
$$

> [!definition] Immagine e controimmagine
Si dice ***immagine di $C \subseteq A$ mediante $f$*** il ***sottoinsieme di B costituito dalle immagini di tutti gli elementi di C***, ovvero:
$$
f(C) := \{b \in B: \exists a \in C : b=f(a)\} = \{f(a): a \in C\}
$$
Si dice ***controimmagine di $C \subseteq B$ mediante $f$*** il ***sottoinsieme di A costituito dagli elementi la cui immagine sta in  C***, ovvero:
$$
f^{-1}(C) := \{a \in A :f(a)\in C\}
$$

Un'applicazione si dice ***suriettiva*** se $\mathrm{Im}(f)=B$.
Un'applicazione si dice ***iniettiva*** se $\forall a_{1},a_{2}\in A\ a_{1}\neq a_{2}\implies f(a_{1})\neq f(a_{2})$.
Un'applicazione ***biiettiva*** è sia *suriettiva* che *iniettiva*, ed è l'unica ***invertibile***, ovvero per la quale si può determinare l'***applicazione inversa*** $f^{-1} : B \to A$ tale che:
$$
\forall a \in A:f^{-1}(f(a)) = a, \forall b \in B:f(f^{-1}(b)) = b
$$
Si dice ***applicazione identica $1_A : A\to A$*** l'applicazione definita come
$$
\forall a\in A: 1_{A}(a) = a
$$
## Composizione
Se $f: A \to B, g: B \to C$ sono due applicazione si dice ***composizione di $f$ e $g$*** l'applicazione $g \circ f:A \to C$ tale che
$$
(g\circ f)(a) = g(f(a)), \forall a \in A
$$
Valgono le seguenti proprietà:
1) $(h \circ g) \circ f = h \circ (g \circ f) : A \to D$, ovvero è associativa;
2) se $f,g$ *iniettive* $\implies g \circ f$ *iniettiva* 
3) se $f,g$ *suriettive* $\implies g \circ f$ *suriettiva* 
4) se $f,g$ *biiettive* $\implies g \circ f$ *biiettiva* 
5) se $g\circ f$ *iniettiva* $\implies f$ *iniettiva*
6) se $g\circ f$ *suriettiva* $\implies g$ *suriettiva*

Risulta quindi che un'applicazione $f: A \to B$ è biiettiva se esiste $g : B \to A$ tale che
$$
g \circ f = 1_{A} \land f \circ g = 1_{B}
$$
e $g$ è l'inversa di $f$.
# Relazioni
Si dice ***relazione*** (*binaria*) **su un insieme $A$** un qualunque **sottoinsieme $\mathcal{R}$ del prodotto cartesiano $A\times A$**. Se $\mathcal{R} \subseteq A \times A$ si usa la notazione $a\mathcal{R}b$ o $a \stackrel{\mathcal{R}}{\equiv}b$ considerata $(a,b)\in \mathcal{R}$ e si dice che $a$ *è in relazione con $b$ rispetto a $\mathcal{R}$*; per indicare la negazione di tale proposizione si inserirà un $\lnot$ prima del simbolo di relazione. Di seguito alcune possibili proprietà:
- ***riflessività***: $\forall a \in A: a\mathcal{R}a$
- ***simmetricità***: $\forall a,b \in A: a\mathcal{R}b \iff b\mathcal{R}a$
- ***transitività***: $\forall a,b,c \in A : (a\mathcal{R}b \land b\mathcal{R}c) \implies a\mathcal{R}c$ 

Una relazione si dice ***d'ordine $\iff$ riflessiva $\land$ anti-simmetrica $\land$ transitiva***
## Equivalenze
Una relazione $\mathcal{E}$ si dice ***equivalenza $\iff$ riflessiva $\land$ simmetrica $\land$ transitiva***. Considerando quindi un'equivalenza $\mathcal{E}$ ed un elemento $a \in A$, si definisce ***classe di equivalenza di $a$ rispetto ad $\mathcal{E}$***:
$$
\overline{a}_{\mathcal{E}} = \{e\in A:a\mathcal{R}e\}
$$
Detti $a,b \in A$ le loro classi godono di varie proprietà:
1) $\overline{a}\neq\overline{b} \implies \overline{a}\cap\overline{b}=\emptyset$;
2) l'unione di tutte le classi di equivalenza è uguale ad $A$.
Date queste due condizioni, l'insieme di tutte le classi di equivalenza costituisce una ***partizione di $A$***. Si definisce $A/\mathcal{E}$ insieme ***quoziente*** e contiene **tutte le classi di equivalenza di $\mathcal{E}$**.
