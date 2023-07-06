---
title: Cluster Analysis
categories:
- Business
feature_image: "https://picsum.photos/2560/600?image=872"
---
Questo progetto è disponibile sottoforma di report [qui](https://github.com/SimoneDeBonis/Projects/raw/main/assets/reports/Cluster%20Analysis.pdf)

La segmentazione della clientela permette di risolvere specifiche esigenze informative a supporto del management aziendale, offrendo all’azienda la possibilità di identificare i propri target e adattare i propri prodotti di conseguenza. Inoltre, permette di calibrare le azioni per massimizzare la soddisfazione del cliente, andando a compiere campagne marketing su misura, che vadano incontro a quelle che sono i bisogni specifici delle categorie individuate. La clientela, infatti, è eterogenea e i consumatori tendono ad avere comportamenti di acquisto e necessità diverse. Per questo è essenziale individuarli, comprenderli, e definire azioni specifiche sulla base di quanto scoperto. 

L’analisi delle 2999 transazioni avvenute tra novembre 2018 e aprile 2019 su un campione di 2583 clienti [1] ha quindi l’obiettivo primario di individuare un ragionevole numero di gruppi distinti, ognuno con caratteristiche discriminanti rispetto agli altri. 

L’algoritmo K-means [2] permette di individuare buyer personas sintetiche per ogni segmento, andando a descrivere in maniera completa tutto il segmento.		 

Sono stati individuati 3 gruppi:

![](https://github.com/SimoneDeBonis/Projects/raw/main/assets/reports/Cluster1.png)

### Gruppo 1  

Nel primo gruppo rientrano 1931 individui, con una media di vendite nette di €6273.  

I clienti che appartengono a questo gruppo tipicamente acquistano solo un prodotto. Tuttavia, se incentivati da opportuni sconti, alcuni di loro hanno acquistato anche quattro volte. 
Infatti, notiamo che questi clienti sono particolarmente sensibili agli sconti durante il Black Friday: le vendite aumentano durante tutto il mese di novembre (39% del totale degli acquisti di questo gruppo). 

Per questo cluster, il tipo di prodotto più acquistato è il prodotto P: è stato oggetto di 1256 transazioni. Per provare a spingere le vendite anche delle altre tipologie di prodotto, si potrebbe attuare una strategia pubblicitaria con prodotti correlati al prodotto P. 

 

### Gruppo 2  

In questo gruppo sono presenti 270 clienti, per 595 ordini, i quali in media spendono €14521. 

Il cliente che ha acquistato di più è ID = 4489293: ha fatto cinque acquisti diversi di importo elevato, in particolare ha acquistato diverse volte il prodotto P, con un valore per ogni transazione di 15834. In presenza di clienti più fedeli rispetto agli altri, come nel caso del cliente con ID = 4489293, si consiglia di rivolgere un’attenzione particolare, ad esempio con messaggi mirati. 

Il tipo di prodotto più interessante per questo cluster è il prodotto P, con 376 vendite. 

Come per il gruppo 1, gli sconti del Black Friday si sono rivelati molto efficaci: il 45% delle vendite sono state effettuate nel mese di novembre. 

### Gruppo 3  

Il presente gruppo individua 380 clienti, i quali hanno realizzato 409 ordini nel periodo considerato. 
In media i clienti effettuano una sola transazione, ma ci sono anche dei fenomeni di riacquisto, come per il cliente con ID = 2593250 che ha effettuato quattro transazioni per il prodotto di tipo A.  

Rispetto agli altri due gruppi, nei quali i clienti sono interessati prevalentemente al prodotto P, quest’ultimo gruppo si caratterizza per l’acquisto del prodotto A. 

Anche in questo caso, la settimana del Black Friday ha portato ad un aumento degli ordini (87% rispetto al totale): in particolare, il gruppo 3 mostra un aumento soltanto nei giorni dell’anno che si caratterizzano per sconti maggiori, sottolineando una sensibilità di questi individui agli incentivi dell’azienda. 

Unendo le informazioni di cui sopra, una scelta supportata dai dati per spronare i clienti di questo gruppo ad acquistare il prodotto A potrebbe essere quella di incentivarli saltuariamente con degli sconti, magari inviando loro dei coupon in specifici periodi dell’anno, si potrebbe attuare una strategia di marketing personalizzata per cliente attraverso Direct E-mail Marketing (DEM) fornendo degli sconti minori nei mesi dove gli acquisti sono meno frequenti e relativi ai prodotti meno acquistati. L'obiettivo è quello di incentivare anche i clienti meno fedeli ed aumentare il profitto derivante dal gruppo 3. 

![](https://github.com/SimoneDeBonis/Projects/raw/main/assets/reports/Cluster2.png)

Considerando il guadagno al netto degli sconti, si evince che il gruppo 2 è quello mediamente più remunerativo nonostante sia il cluster con minor numero di utenti. Dunque, i clienti individuati in questo gruppo meritano una particolare attenzione da parte dell’azienda, per incentivare un possibile riacquisto futuro del prodotto. 

Inoltre, si conferma che il gruppo 3 si differenzia dagli altri in quanto apporta un contributo minore all’azienda: i dati sembrano suggerire che questo gruppo di individui sia particolarmente sensibili agli sconti, i cui acquisti avvengono soltanto nei periodi dell’anno prossimi alle festività e ad eventi come il Black Friday. 

### Appendice 

[1] Valori anomali: 

Durante la nostra analisi sono emersi due clienti con un comportamento eterogeneo rispetto agli altri, in particolare i clienti ID = 9533448 e ID = 4189899 che hanno effettuato, rispettivamente, tre e un reso, ossia la totalità dei resi di tutti i clienti. L’analisi della clientela si è focalizzata, invece, sulla clientela che effettua ordini senza fare il reso del prodotto; perciò, questi due valori anomali sono stati eliminati prima di effettuare il raggruppamento. 

[2] Numero ottimale di Cluster 

Il numero di cluster nel K-means è stato individuato mediante la combinazione di elbow method e analisi della silhouette, in modo tale da ottenere un numero ragionevole di gruppi. 

### Il team

Damiano Agachi Menna [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/damiano-am/)  
Annalisa Basta [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/annalisabasta/)  
Simone De Bonis [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/SimoneDeBonis)  
Chiara Mercati [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/chiara-mercati-476b07275/)  
Daniele Torregiani [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/daniele-torregiani-369b54243/)  