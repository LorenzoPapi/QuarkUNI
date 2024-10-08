Deriva dal nome del matematico persiano ***al-Khwarizmi*** che scrisse per primo di queste procedure. Indica una sequenza di regole o istruzioni che permette di ***risolvere un [[01 - Informatica#Problemi|problema]]*** e valgono le proprietà di:
- ***Definitezza***: ogni azione deve essere **univocamente determinata**;
- ***Eseguibilità***: ogni azione deve essere **eseguibile**;
- ***Finitezza***: deve contenere un **numero finito di azioni**, eseguite ciascuna in un **tempo finito** per un **numero finito di volte**;
- ***Generalità***: risolve una *classe* di problemi, non le singole istanze, quindi **è indipendente dall'input**.

Gli algoritmi sono descritti con un **linguaggio e dettaglio** delle azioni che dipendono dalle **capacità dell'esecutore**, instaurando una relazione biunivoca tra la **macchina M** e il **linguaggio L** scelto. Un particolare esecutore che si considera è il ***calcolatore elettronico***, detto *computer*, ed il ***programma*** è un **testo** scritto secondo **sintassi e semantica** del linguaggio, la **formulazione testuale** dell'algoritmo scelto per risolvere il problema.

> Problema -> algoritmo (tramite metodo risolutivo) -> programma (tramite linguaggio)

Nella risoluzione quindi ci sono **aspetti metodologici**:
- *formalizzare* il problema;
- *analizzare* il problema e *identificare* la soluzione (***pensiero computazionale***);
- *formalizzare la soluzione* e definire l'*algoritmo risolutivo*;
e **tecnologici**:
- *scrittura* in un *linguaggio di programmazione*;
- *esecuzione* del programma;
- *valutazione e correzione*.

Si rappresentano per via **grafica** tramite i **[diagrammi di flusso](draw.io)** o via **testuale** tramite lo **pseudo-codice**. Le *istruzioni* di base sono:
- *Trasferimento di informazione* (***I/0***): lettura iniziale, scrittura finale, visualizzazione intermedia;
- *Esecuzione di calcoli*: **valutazione di espressioni aritmetiche**;
- *Assegnamento*: permette la definizione di ***variabili***;
- *Controllo*: modificano il **flusso** delle operazioni.
![[02-01.png]]
Una ***variabile*** è una coppia **(nome, valore)** che serve a **memorizzare l'informazione** in *ingresso, intermedio e fine*. Si può attribuire valore ad essa o tramite **inizializzazione** o tramite **lettura da input**.

I diagrammi di flusso hanno dei limiti causati dalla loro natura: data la natura **grafica bidimensionale**, per progetti grandi diventano ingestibili, data la grande quantità di frecce. Da un lato possono servire per un *livello generale* dell'algoritmo, o per parti *estremamente particolari.