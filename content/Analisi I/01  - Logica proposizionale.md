Il linguaggio matematico è composto da **proposizioni**, fondamento dei **ragionamenti**. È proposizione qualsiasi enunciato di senso compiuto a cui si può assegnare un **valore di verità** (V o F). Il ragionamento è la concatenazione di proposizioni tramite **connettivi logici**. Per essere utile deve essere necessariamente **corretto formalmente** ma la sua **correttezza reale** dipende dalla verità delle premesse: un ragionamento formalmente corretto può essere falso se una o più delle sue premesse sono false.
## Connettivi logici
Sono elementi che prendono una o più proposizione per condensarle in un'altra detta **conclusione**. Il loro funzionamento si descrive tramite le **tabelle di verità**. I principali sono:
- **negazione logica** $\lnot p$ (unaria);
- **congiunzione logica** $p \land q$ (binaria, commutativa);
- **disgiunzione logica** $p \lor q$ (binaria, commutativa);
- **disgiunzione esclusiva logica** $p \oplus q$ (binaria, commutativa);
- **implicazione logica** $p \implies q$ (binaria).

| $p$ | $q$ | $p \land q$ | $p \lor q$ | $p\oplus q$ | $p \implies q$ |
| --- | --- | ----------- | ---------- | ----------- | -------------- |
| V   | V   | V           | V          | F           | V              |
| V   | F   | F           | V          | V           | F              |
| F   | V   | F           | V          | V           | V              |
| F   | F   | F           | F          | F           | V              |

| $p$ | $\lnot p$ | $\lnot p \land p$ | $\lnot p \lor p$ |
| --- | --------- | ----------------- | ---------------- |
| V   | F         | F                 | V                |
| F   | V         | F                 | V                |

**Esempio di implicazione**
>Avendo due mazzi da 52 carte di dorso rosso e blu, si mischiano. Affermo che il mazzo ottenuto ha la seguente proprietà: il dorso di tutte le carte di cuori è rosso. Prendendo cinque carte: asso di picche, asso di cuori, asso di quadri, carta girata dorso rosso, carta girata rosso blu. Quante devo girarne per vedere se l'affermazione è vera?

*Risposta*: ne bastano due, quella di cuori e quella blu. Si afferma che $C \implies R$, che è falsa solo per $C\land\lnot R$. Quindi basta controllare la carta di cuori per vederne il dietro, e controllare se dietro il blu c'è un cuore o no.
### Regole
1) $p\equiv q$ significa che $p$ e $q$ hanno la stessa tabella di verità, ovvero sono **equivalenti**;
2) $\lnot(\lnot p) \equiv p$ (doppia negazione);
3) $\lnot p \lor p \equiv T$ (principio del terzo escluso, **tautologia**);
4) $\lnot p \land p \equiv F$ (**contraddizione**);
5) $\lnot(p \lor q) \equiv \lnot p \land \lnot q$ (1° legge di de Morgan, p = sto al mare, q = nuoto);
6) $\lnot(p \land q) \equiv \lnot p \lor \lnot q$ (2° legge di de Morgan, p = sto in montagna, q = scio);
7) $\lnot(p\implies q) \equiv p \land \lnot q$ (p = piove, q = mi bagno)
#### Conseguenze
1) $p \implies q \equiv \lnot(\lnot(p\implies q)) \equiv \lnot(p \land \lnot q) \equiv \lnot p \land q$
2) $p \implies q \equiv \lnot p \land q \equiv \lnot (\lnot q) \land \lnot p \equiv \lnot q \implies \lnot p$ (**contronominale**)