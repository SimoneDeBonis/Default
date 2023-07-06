---
title: Previsione deli ricavi di Apple
categories:
- Business
feature_image: "https://picsum.photos/2560/600?image=872"
---
Questo progetto è disponibile sottoforma di report [qui](https://github.com/SimoneDeBonis/Projects/raw/main/assets/reports/Ricavi%20Apple.pdf)


Per una società, la conoscenza dei suoi ricavi futuri rappresenta un’informazione di altissimo valore perché permette di intervenire tempestivamente sulle scelte strategiche assunte in precedenza e di regolare i propri investimenti. Inoltre, per l’investitore queste informazioni sono fondamentali per decidere se investire o meno. 

Inizialmente abbiamo individuato i fattori che potenzialmente influenzano i ricavi della società Apple[1], perciò, oltre a considerare i dati storici della serie di riferimento dal primo trimestre 1998 e al quarto trimestre 2021, abbiamo considerato anche alcune variabili macroeconomiche:  

- Prodotto Interno Lordo dei Paesi emergenti: esprime il valore aggregato di beni e servizi finali prodotti nei paesi emergenti a prezzi di mercato.  
Abbiamo scelto uno degli indicatori chiave dello sviluppo economico dei Paesi emergenti 	perché nelle altre regioni come l’Europa o l’America il mercato potrebbe essere già arrivato 	a saturazione; quindi, riteniamo che la maggior parte della crescita attuale potrebbe 		derivare dall’aumento della domanda proprio da questi Paesi. 

- Produzione Industriale: la produzione reale di tutti gli stabilimenti negli Stati Uniti.  

In aggiunta, abbiamo considerato le materie prime usate per produrre le componenti dei dispositivi elettronici: 

- Alluminio 
- Rame

Nell’analisi abbiamo considerato anche le azioni della principale azienda fornitrice di Apple e delle altre multinazionali del settore, che produce la maggior parte dei microprocessori: 

- Valore azionario di TSMC: Taiwan Semiconductor Manufacturing Company 

Per svolgere la seguente analisi abbiamo deciso di implementare SVR: Support Vector Regression.  

### Modello: 

Il modello è un SVR con kernel lineare [2].  

Alcuni dei regressori presi in considerazione si sono rilevati influenti sui ricavi Apple con un periodo di ritardo: le azioni di TSMC, la produzione industriale, il valore del rame e il PIL dei Paesi emergenti mostrano degli effetti significativi sui ricavi a partire dal trimestre successivo [3] mentre l’alluminio ha un effetto immediato. 

Inoltre, per predire i ricavi futuri è stata utilizzata anche la serie storica dei ricavi stessi di Apple con un lag di un periodo. 

![](https://github.com/SimoneDeBonis/Projects/raw/main/assets/reports/SVR1.png)

Dall’analisi del modello notiamo che i ricavi di Apple per i quattro trimestri del 2022 aumenteranno, considerando un intervallo di confidenza entro il quale il valore predetto potrebbe oscillare. 

<img src="https://github.com/SimoneDeBonis/Projects/raw/main/assets/reports/SVR2.png" width="700" height="200"/>

### Implicazioni di Business: 

Come visibile dal grafico, i valori di previsione futura presentano una crescita notevole rispetto agli ultimi dati disponibili. Questo trend positivo è presente anche considerando soltanto i minimi della “forchetta” di previsione (intervallo di confidenza inferiore al 5%). In particolare, mantenendo inalterate le condizioni dell’analisi, la variazione annuale dei ricavi del 2022 rispetto al 2021 (in %) stimata dal modello si attesta tra +17.63% e +26.22%, con un tasso medio di crescita del +21.93%. 

Queste informazioni suggeriscono una buona opportunità di investimento in Apple nel breve periodo (1 anno). Tuttavia, com’è noto, considerare soltanto i ricavi può fornire una visione parziale della società. 

Per una valutazione complessiva e consapevole, l’analisi dei ricavi futuri e della loro variazione percentuale andrebbe correttamente integrata con considerazioni accurate in merito alla sua solidità finanziaria e patrimoniale, e confrontata con lo stato delle altre aziende dello stesso settore, valutando eventuali sopravvalutazioni con altri indicatori (ad esempio il rapporto Prezzo/Utili).  

### Possibili analisi future: 

Durante la valutazione delle informazioni da considerare per la costruzione del modello, sono emerse delle relazioni interessanti tra i ricavi di Apple ed il valore generato dai servizi che la società offre. In particolare, riteniamo influenti i ricavi derivanti: dalle applicazioni che si trovano nell’Apple Store, dai servizi offerti come ad esempio Apple Music, dalla possibilità di pagamento integrato e dalla possibilità di aprire un conto di risparmio Apple Savings. Sfortunatamente i dati relativi a questi servizi sono pochi e molto recenti: riteniamo perciò che queste informazioni potrebbero essere usate come regressori per analisi future

### Appendice: 

[1] **Trasformazione delle variabili in log-diff e test di stazionarietà**:  

Al fine di garantire la stazionarietà della variabile dipendente e un ordine di grandezza adeguato dei regressori, abbiamo trasformato tutte le variabili originarie usate nel modello con la log-differenziazione. Successivamente, la stazionarietà delle variabili trasformate è stata verificata attraverso i test ADF e KPSS. 

[2] **Modello** 

Per individuare gli iperparametri del modello abbiamo svolto una cross-validation [sliding-window?] minimizzando l’MSE (Mean Square Error). In base ai dati scelti per il modello, questa tecnica ha suggerito l’uso di un kernel lineare con con iperparametro C, costo di misclassificazione, pari a 41. 

[3] **Ritardi e selezione dei regressori**

La costruzione del modello è stata preceduta dalla considerazione delle variabili da utilizzare. 

Dopo aver individuato un ampio insieme di variabili micro e macroeconomiche potenzialmente rilevanti ad influenzare i ricavi Apple, abbiamo applicato ad esse un ritardo di due periodi. L’uso dei ritardi anche per la feature selection è motivato dall’idea di ricercare le correlazioni tra le covariate e la variabile di interesse con l’ottica di costruire un modello realmente predittivo. 

### Il team

Damiano Agachi Menna [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/damiano-am/)  
Annalisa Basta [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/annalisabasta/)  
Simone De Bonis [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/SimoneDeBonis)  
Chiara Mercati [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/chiara-mercati-476b07275/)  
Daniele Torregiani [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/daniele-torregiani-369b54243/)  