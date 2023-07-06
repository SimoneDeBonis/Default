---
title: Estimating future EPS using Lasso Regression
categories:
- Business
excerpt: |
  A pot still is a type of still used in distilling spirits such as whisky or brandy. Heat is applied directly to the pot containing the wash (for whisky) or wine (for brandy).
feature_text: |
  ## The Pot Still
  The modern pot still is a descendant of the alembic, an earlier distillation device
feature_image: "https://picsum.photos/2560/600?image=733"
image: "https://picsum.photos/2560/600?image=733"
---

Questo progetto è disponibile sottoforma di report [qui](https://github.com/SimoneDeBonis/Projects/raw/main/assets/reports/Regressione%20Lasso.pdf)

La stima dell’EPS futuro è un’informazione fondamentale per un investitore: permette sia di indurre il potenziale ritorno sull’investimento ottenibile investendo in una specifica società, sia di comparare la redditività di aziende diverse. 
La regressione è una tecnica di analisi statistica che permette di indagare relazioni di dipendenza tra variabili e consente di studiare i rapporti causa-effetto: attraverso la regressione è possibile analizzare la dinamica dei profitti delle aziende e stimare l’EPS futuro di un’impresa, questo significa poter decidere se far parte del suo azionariato oppure no.
Le informazioni disponibili su 2482 [1] società presenti nell’indice Russell 3000 comprendono le rispettive categorie e sottocategorie industriali di appartenenza, oltre ai valori di alcuni indicatori economici e finanziari. Il dataset presenta una notevole variabilità in ognuno degli indicatori, con differenze marcate in base al settore industriale. Ad esempio, le società appartenenti al settore “Consumer Discretionary”, in media, hanno elevati livelli di ROE e di Vendite Nette. 
Le informazioni disponibili su 2482 [1] società presenti nell’indice Russell 3000 comprendono le rispettive categorie e sottocategorie industriali di appartenenza, oltre ai valori di alcuni indicatori economici e finanziari. Il dataset presenta una notevole variabilità in ognuno degli indicatori, con differenze marcate in base al settore industriale. Ad esempio, le società appartenenti al settore “Consumer Discretionary”, in media, hanno elevati livelli di ROE e di Vendite Nette
A partire da queste è stato possibile sviluppare il modello di regressione ad hoc con l’obiettivo principale di comprendere la dinamica dei profitti aziendali. 
Il modello è stato definito in modo tale che l’errore di generalizzazione sia il minore possibile, ma anche facendo attenzione alla sua parsimonia, ovvero evitando di inserire un numero troppo elevato di variabili non informative.  
Partendo dalle variabili disponibili, e considerando anche la loro combinazione fino al quarto grado, si è implementato l’algoritmo LASSO per la selezione delle variabili più significative. Alla luce delle suddette analisi, il modello che meglio rappresenta il fenomeno è [2]: 

![](https://github.com/SimoneDeBonis/Projects/raw/main/assets/reports/Lasso1.png)
![](https://github.com/SimoneDeBonis/Projects/raw/main/assets/reports/Lasso2.png)


Il modello contiene informazioni quantitative sugli indicatori maggiormente influenti rispetto alle stime dell’EPS futuro (come l’Enterprise Value, il Return On Asset, e le interazioni presenti tra EV - ROE e NS – ROA), ma anche le informazioni qualitative sulle categorie industriali.
Nell’equazione del modello è presente l’intercetta, all’interno della quale troviamo anche informazioni riguardo il settore ‘Basic Materials’ [3]. 
In aggiunta alle variabili fornite, sono state considerate combinazioni lineari e non tra le stesse, delle quali si sono rivelate maggiormente significative le seguenti:
-	Enterprise Value • Return On Equity
Il valore dell’impresa, moltiplicato per la redditività del capitale investito, ha un’influenza negativa sull’EPS: ciò significa che all’aumentare di questo prodotto di una unità, l’EPS diminuisce di 0.21, mantenendo costanti gli effetti delle altre variabili.
-	Net Sales • Return On Asset
Le vendite nette dell’impresa, moltiplicate per la redditività della stessa in relazione alle risorse utilizzate per svolgere la propria attività economica ha un’influenza positiva sull’EPS. Questo significa che all’aumentare di questo prodotto l’EPS aumenta di 0,41. 

 Al fine di utilizzare il modello per scopi inferenziali, cioè prevedere in modo affidabile i valori futuri della variabile target, è necessario che lo stimatore OLS del fenomeno analizzato sia consistente. Questo implica che devono essere verificate le condizioni di indipendenza lineare tra i regressori, una distribuzione omoschedastica dei residui e le variabili esplicative devono essere incorrelate con gli errori del modello.
Nel caso specifico, i coefficienti stimati ci permettono di spiegare la variabile dipendente ma non di fare previsioni in modo efficiente e robusto [4].
Sviluppi Futuri: 
Considerando i limiti di cui sopra, sono necessari ulteriori approfondimenti per poter sviluppare un’analisi robusta: la distorsione da variabili omesse può essere mitigata includendo nuove variabili che ben si prestano a descrivere il fenomeno come, per esempio, il numero di azioni circolanti. 
Includendo più istanze storiche per ciascuna variabile si potrebbe ridurre la distorsione da campionamento, andando ad indagare il fenomeno nel suo complesso piuttosto che limitandosi al semplice anno in esame.

### Appendice 
[1] Valori duplicati e anomali:
Durante l’analisi sono emersi 11 valori duplicati, per la stessa società erano presenti due righe con valori uguali per tutti gli attributi, con differenze solo per il campo “Net_Sales”, e per l’analisi è stato selezionato il valore più realistico.
Inoltre, è stato osservato che per determinati attributi sono presenti valori molto grandi e lontani dalla realtà, abbiamo quindi sostituito il valore anomalo con una media della sottocategoria dell’industria riferita a quel determinato attributo.
Ridondanza: 
Durante l’analisi descrittiva, attraverso un correlogramma, abbiamo notato che alcune variabili erano fortemente correlate: abbiamo comunque deciso di prenderle in considerazione per l’analisi.    






[2] Coefficienti regressione:
La costruzione del modello ha richiesto diversi passaggi: 
-	Le variabili sono state standardizzate, dopodiché sono stati calcolati i prodotti incrociati, i quadrati e i cubi delle stesse;
-	È stato utilizzato uno stimatore Lasso per identificare le variabili più importanti, l’iperparametro λ è stato individuato attraverso una 10-fold cross-validation con l’algoritmo Cyclical Coordinate Descent (CCD);
-	Sulle variabili individuate dalla regressione lasso è stato utilizzato un OLS.
![](https://github.com/SimoneDeBonis/Projects/raw/main/assets/reports/Lasso3.png)

[3] Multicollinearità:
Per evitare il problema della multicollinearità, nel modello sono state inserite n-1 variabili dummy (dove n è il numero di settori presenti), perciò il β relativo a Basic Materials è contenuto nell’intercetta, e tutte le altre variabili sono espresse in funzione della distanza da Basic Materials.
[4] Consistenza dei coefficienti:
Data la complessità e la variabilità del fenomeno oggetto di studio, basandosi esclusivamente sulle covariate disponibili, si segnala un problema di potenziale mispecificazione (il RESET test rifiuta l’ipotesi nulla per tutte le possibili combinazioni di variabili, anche non lineari fino al terzo ordine) e, potenzialmente, di variabili omesse. Questo condurrebbe alla non consistenza dello stimatore OLS. Ciò significa che le stime del modello sono comunque indicative allo scopo di spiegare l’influenza che hanno le covariate sulla dinamica dell’EPS futuro, ma significa anche che i valori reali potrebbero scostarsi da quelli stimati.
Per questo motivo abbiamo evitato di eseguire test di inferenza statistica sui parametri stimati.

### Il team

Damiano Agachi Menna [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/damiano-am/)  
Annalisa Basta [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/annalisabasta/)  
Simone De Bonis [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/SimoneDeBonis)  
Chiara Mercati [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/chiara-mercati-476b07275/)  
Daniele Torregiani [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/daniele-torregiani-369b54243/)  