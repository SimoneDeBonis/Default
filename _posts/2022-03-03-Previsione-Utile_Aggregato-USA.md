---
title: Previsione dell'utile aggregato delle aziende americane
categories:
- Business
feature_image: "https://picsum.photos/2560/600?image=872"
---
Questo progetto è disponibile sottoforma di report [qui](https://github.com/SimoneDeBonis/Projects/raw/main/assets/reports/Time%20Series%20Report.pdf)


L’utile di un’impresa è uno degli indicatori più importanti per fare analisi di mercato, aiuta a comprendere quanto una società sia redditizia. 
Conoscere in anticipo l’utile aggregato futuro porta vantaggio competitivo dal momento che permette di prendere decisioni di business in modo consapevole, capendo se avviare una nuova società potrebbe rivelarsi un investimento profittevole o meno. 

Per sviluppare un’analisi predittiva sull’utile delle imprese americane, oltre a considerare i dati storici della serie di riferimento dal primo trimestre 1990 e al terzo trimestre 2022, abbiamo considerato in aggiunta anche alcune variabili macroeconomiche:1 

- Oro: dinamica del prezzo dell’oro in dollari per oncia.  

- Indice di produzione: misura la produzione reale di tutti gli stabilimenti negli Stati Uniti.  

- Tasso di riferimento: si riferisce al tasso di interesse con il quale gli Istituti di credito si scambiano tra loro fondi federali, detenuti presso la Federal Reserve. 

- Indice di fiducia dei consumatori (CCI): è un sondaggio mensile che misura il grado di ottimismo dei consumatori verso l’economia, e le loro aspettative per il futuro; 

- Crash: è una variabile dummy, inserita per prendere in considerazione la crisi finanziaria del 2008 dopo il fallimento di Lehman Brothers (3° e 4° trimestre 2008, 1° trimestre 2009). 

- Covid: una variabile dummy, inserita per considerare gli effetti della crisi economica dovuta al recente fenomeno epidemiologico (1° e 2° trimestre 2020). 

- War: una variabile dummy, per tenere conto dei ribassi nell’economia globale a seguito dello scoppio della guerra in Ucraina (2° e 3° trimestre 2022). 

Modello [1]: 

Dall’analisi del modello notiamo che la crescita del prezzo dell’oro è correlata negativamente con l’aumento degli utili; perciò, quando il prezzo dell’oro diminuisce si notano degli effetti al rialzo sugli utili già dopo 3 mesi. Questo potrebbe essere spiegato dal fatto che l’oro è un bene rifugio, il quale non è sottoposto a svalutazione e su cui le persone investono in periodi di incertezza economica. Inoltre, anche l’indice di confidenza dei consumatori è risultato particolarmente interessante, perché notiamo che l’ottimismo dei consumatori, statisticamente significativo, mostra un impatto positivo sugli utili a distanza di 6 mesi. 

Abbiamo svolto l’analisi predittiva in base a tre possibili scenari futuri per tutto il 2023 [2]: 

### Scenario Pessimista

![](https://github.com/SimoneDeBonis/Projects/raw/main/assets/reports/time1.png)

Il primo scenario si riferisce ad una condizione estremamente negativa, dove assistiamo ad un crollo degli utili più che consistente, a seguito degli effetti sull’economia di una potenziale crisi finanziaria e della guerra: a seguito di questo shock, gli utili previsti appaiono dimezzati dopo appena 6 mesi (dal terzo trimestre 2022 al primo del 2023), per poi diminuire ancora durante il corso dell’anno, fino ad arrivare ad un valore atteso di $40 miliardi a chiusura dell’esercizio.  

In questo scenario consigliamo di rimanere vigili alle possibili opportunità di mercato che si generano nei momenti immediatamente successivi alle crisi, per sfruttare al massimo l’eventuale ripresa economica e l’ottimismo dei consumatori. In ogni caso, sempre tenendo a mente i potenziali rischi che questa soluzione porta con sé. 

### Scenario Atteso 

![](https://github.com/SimoneDeBonis/Projects/raw/main/assets/reports/time2.png)

Descrizione generata automaticamenteIn caso di uno scenario futuro “neutrale” privo di shock, il valore atteso degli utili futuri ad un anno è in lieve aumento rispetto al terzo trimestre 2022, passando da 187 a 198 mld USD (+ 5.88%). 

Successivamente, il modello prevede che gli utili delle società USA quotate a fine 2023 cresceranno con circa il 55% di probabilità.  

In particolare, la forbice di valori predetti oscilla tra i 166 e i 234 mld USD con una probabilità del 90% (quindi tra - 11.22% e + 25.13% rispetto al terzo trimestre 2022). 

In questa situazione, avviare un’impresa negli Stati Uniti può sembrare una decisione favorevole nel breve periodo. Tuttavia, occorre sempre tenere in considerazione i rischi dell’avvio di un’attività in un settore già consolidato: inizialmente potrebbero esserci alcuni fattori che andranno a limitare i guadagni, come gli ingenti investimenti per l’avvio dell’impresa, le barriere all’ingresso presenti nel settore e alcune azioni ostili delle imprese già esistenti sul mercato mirate a limitare la concorrenza. 

### Scenario ottimista

![](https://github.com/SimoneDeBonis/Projects/raw/main/assets/reports/time3.png)

Nel terzo scenario di previsione per il 2023 consideriamo una possibile crescita economica.  

Il valore atteso degli utili delle imprese americane, in queste condizioni favorevoli, è stimato intorno ai $203 miliardi nel primo trimestre del 2023, fino ad arrivare a $224 miliardi alla chiusura dell’esercizio. 

Inoltre, secondo il modello in questa situazione a fine 2023 gli utili saranno superiori ad almeno 190 mld USD con una probabilità del 90%, e potrebbero arrivare potenzialmente fino a 258 miliardi. 

Questo scenario è sicuramente il più favorevole. Sarebbe opportuno tenere sotto controllo le dinamiche delle 4 variabili esogene scelte. Ad esempio, un buon momento per avviare l’attività si presenta quando il CCI di 6 mesi precedenti varia a rialzo di circa +3%, la produzione industriale del trimestre precedente cresce di almeno +1%, il prezzo dell’oro cala (almeno di 50-70$ l’oncia rispetto al trimestre precedente) e le aspettative sulle variazioni del tasso di riferimento per il prossimo trimestre restano stabili, ovvero non vanno oltre +/- 0.05. 

### Appendice

Il modello usato per le previsioni è un ARIMAX(1, 1, 1), la cui variabile dipendente è l’utile trimestrale. È stato scelto in base al minor BIC, tenendo conto delle 4 variabili esogene differenziate e con ritardo ad 1 o 2 periodi per rendere il modello realmente “previsivo”. Le 3 dummy sono state aggiunte per considerare l’impatto negativo degli eventi straordinari sugli utili. 

L’integrazione di ordine 1 nell’ARIMAX rende stazionaria la serie degli utili, così come confermato dai test di radice unitaria ADF, PP e KPSS. 

Inoltre, i test diagnostici eseguiti sul modello non segnalano problemi di errata specificazione (Test LM di ordine 4 per l’autocorrelazione non rifiuta la nulla), e neanche problemi di eteroschedasticità condizionale (Test ARCH di ordine 4 non rifiuta l’ipotesi di omoschedasticità dei residui).   

Inoltre l’ARIMAX(1,1,1), è il modello che, data la scelta delle 4 esogene, riduce l’RMSE out-of-sample del 2023 a 7.27 (in questo caso usando come training set le osservazioni fino a 2021:4). 

 I coefficienti stimati con Massima verosimiglianza esatta per la variabile dipendente I(1) ∆ 〖Utile〗_t sono:

![](https://github.com/SimoneDeBonis/Projects/raw/main/assets/reports/time4.png)

[2] Costruzione degli scenari 

Scenario ottimista: considerata la stessa variazione del 2021, in una situazione in cui non ci sono crisi e gli effetti della guerra sull’economia sono svaniti. In particolare, assumiamo non solo un completo riassorbimento dell’impatto negativo della guerra sugli utili previsti, ma anche che ci sarà una crescita tipica dei periodi post-crisi. 

Scenario pessimista: considerata la stessa variazione del 2008/inizio del 2009, per prevedere quale sarà l’andamento degli utili in una situazione di crisi, inserendo gli effetti considerati con le variabili dummy crash e guerra. Ipotizziamo per il 2023 una situazione macroeconomica fortemente negativa, causata da una possibile crisi finanziaria e dal susseguirsi degli effetti negativi della guerra in Ucraina anche sugli utili delle società americane. 

Scenario atteso: considerata la stessa variazione del 2019, inserendo gli effetti sugli utili della guerra, ma in una situazione di stabilità, ossia dopo lo shock iniziale. 

Perciò, sia nello scenario ottimista che nello scenario neutro, anche se la guerra prosegue, gli effetti sugli utili sono mitigati.  

### Il team

Damiano Agachi Menna [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/damiano-am/)  
Annalisa Basta [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/annalisabasta/)  
Simone De Bonis [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/SimoneDeBonis)  
Chiara Mercati [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/chiara-mercati-476b07275/)  
Daniele Torregiani [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/daniele-torregiani-369b54243/)  