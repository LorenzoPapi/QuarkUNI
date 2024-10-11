L'**informatica** è la scienza della ***rappresentazione ed elaborazione automatica dell'informazione*** (*Computer science* è sugli elaboratori, *Information science* è sull'informazione):
- *scienza* perché è una **conoscenza *sistematica* e *rigorosa*** di tecniche;
- ***informazione*** è l'**oggetto dell'indagine**;
- **rappresentazione** è come l'informazione viene **strutturata e trasformata**;
- **elaborazione automatica** è l'uso dell'informazione per uno scopo, e deve essere **eseguibile** in maniera automatica.

Comprende:
- metodi per **rappresentare** l'informazione e le **soluzioni**;
- **linguaggi di programmazione**;
- **[[04 - Architettura dei calcolatori|architettura dei calcolatori]]**;
- **sistemi operativi**;
- **reti di calcolatori**;
- **calcolo numerico**;
- **[[02 - Algoritmi|algoritmi]]**.

L'attività dell'**ingegnere informatico** è trovare la **soluzione a un problema** e formalizzarla in maniera tale da farla poter eseguire da un **calcolatore**.
## Problemi
Un ***problema*** è un quesito a cui si vuole **dare una risposta** o un **obiettivo da perseguire**, ed è quindi **soggettivo**. Di tutti i problemi esistenti, quelli **risolvibili in maniera automatica** sono quelli definibili in modo **preciso**, **univoco** e **non ambigua**, e quindi che possono essere tali per tutti. In particolare un problema si dice ***ben formulato*** (formalmente definito) se:
- è **comprensibile** al calcolatore;
- sono presenti **dati a sufficienza** per determinarne la soluzione;
- il criterio di verifica è **univoco** (*è noto il contesto*).

I problemi vanno **formalizzati** in maniera matematica e molto spesso bisogna **analizzarli** per capire la tipologia di **dati** e **risultati**, anche a seconda delle capacità dell'esecutore. Infine, spesso si parla di ***classe* di problemi**, piuttosto che di *singole istanze*:

> *Classe*: determinare l'area di un rettangolo di lati $a$ e $b$
> *Istanza*: determinare l'area di un rettangolo di lati 3 e 4 cm.
### Risolvibilità
***Risolvere*** un problema significa **ricercare e descrivere con un** <b><u><i><span title='Formalismo.'>linguaggio di programmazione</span></b></u></i> un [[02 - Algoritmi|algoritmo]] che, eseguito, consenta partendo dai <b><u><i><span title="'L'input.">dati</span></b></u></i> di ottenere dei <b><u><i><span title="L'output.">risultati</span></b></u></i> che soddisfano un <b><u><i><span title='Metodo di controllo per affermare la correttezza dei risultati ottenuti a partire dai dati.'>criterio di verifica</span></b></u></i>.

Il ***solutore*** è il **soggetto** che mediante un linguaggio **descrive la soluzione del problema** ad un ***esecutore*** capace di eseguire un insieme di <b><i><u><span title='Comandi elementari.'>istruzioni</span></u></i></b> su un insieme di oggetti per ottenerne un altro.

I problemi ***risolvibili*** sono quelli per cui è **noto che *esiste un procedimento risolutivo***, quelli ***risolvibili?*** ***non* è noto se esiste**, quelli ***irrisolvibili* è noto che *non esiste soluzione***.