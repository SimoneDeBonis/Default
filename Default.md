---
title: Early Warning del default dei comuni
feature_text: 
feature_image: "https://simonedebonis.github.io/Projects/assets/PowerBI/napoli.jpg"
excerpt: "A demo of Markdown and HTML includes"
aside: false
---


### Obiettivo dell'analisi

Il **default**, meglio definito come **dissesto finanziario** si verifica quando un comune caratterizzato da gravi ed incontrovertibili condizioni di squilibrio finanziario non riesce più a svolgere le sue funzioni di base e a fornire alla cittadinanza quei servizi considerati indispensabili. 
Il dissesto di un comune è una cosa ben diversa dal fallimento di un’impresa privata: non si può determinare l’estinzione perché́ gli enti locali non possono cessare di esistere, bisogna garantirne la continuità̀ amministrativa. 
Il dissesto è una procedura complessa che impatta negativamente sulla qualità della vita dei suoi cittadini: comprendere perché questo succeda è fondamentale per prevenirlo agendo tempestivamente. 
L’analisi si concentra sull’anno 2018.


### IL dataset 

Il dataset è stato realizzato aggregando i dati necessari da più fonti: ISTAT, Ministero dell’Interno, dalla Circolare 20/2020 dell’Ufficio I Consulenza e studi finanza locale è stato possibile ottenere i comuni dissestanti o deficitari fino all’anno 2019.
OpenCivitas:
- la politica di coesione del Fondo Sviluppo e Coesione (ex FAS) che, attraverso risorse
nazionali, finanzia progetti strategici, sia di carattere infrastrutturale sia di carattere
immateriale, di rilievo nazionale, interregionale e regionale.
- il fondo perequativo è uno strumento che mira a mitigare le diseguaglianze tra
Regioni i cui abitanti presentano differenti capacità fiscale, al fine di garantire gli stessi standard di prestazione nell’erogazione dei servizi di competenza, nonostante gli squilibri economico-sociali: il fondo è istituito senza vincolo di destinazione ed è finanziato da quote di entrate tributarie.
MEF/Dipartimento delle finanze:
- ricavando i dati Irpef degli enti locali ha reso possibile aggiungere la variabile che
tenesse conto del reddito imponibile individuale per ciascuno di loro.

Il dataset finale è composto da:

- **Variabili sociali**: il genere, l’età e l’istruzione del sindaco, il numero di abitanti medi nel periodo 2012-2018. L’utilizzo a fini di analisi del partito politico di appartenenza del sindaco è limitato dalla presenza massiccia di liste civiche non riconducibili alle aree politiche di appartenenza.
- **Variabili finanziarie**: Fondo Perequativo, Fondo Storico, Rimborso prestiti su entrate correnti, Rigidità della spesa, Reddito imponibile individuale, Consistenza iniziale dei residui passivi, Popolazione media, Spese personale su spese correnti, Grado di finanziamento interno, Dipendenza da finanziamento esterno, Dipendenza da contributi e trasferimenti correnti ed Autonomia impositiva.

![](/assets/PowerBI/plots.png)

In alcuni dataset mancano i dati relativi alle regioni a statuto speciale come le isole.

### Analisi Sociale

![](/assets/PowerBI/power1.png)

Cominciamo analizzando la situazione sociale dei comuni italiani, possiamo filtrare per regione, provincia, popolazione ed età , sesso o titolo di studio del sindaco, nonchè popolazione residente.
Il KPI in alto mostra la percentuale di sindache sul totale.
I  Grafici a barre mostrano la distrubzione di sindaci/sindache e dei loro titoli di studio 
la mappa in alto a destra mostra la densità della popolazione che è molto simile a quella delle [centrali elettriche](https://simonedebonis.github.io/Projects/Qlik/), come atteso.

![](/assets/PowerBI/power1.1.png)

Possiamo focalizzare la nostra analisi su una singola provincia come, ad esempio, quella di Ancona.
Andando sul singolo comune possiamo visualizzarne le caratteristiche nel dettaglio, dalle caratteristiche del sindaco alla differenza di popolazione tra il 2018 e il 2011, in media tutti i comuni italiani sono affetti da spopolamento
La percentuale di sindaci di sesso femminile è maggiore al nord () e nei comuni con sindaci più giovani ()

![](/assets/PowerBI/power1.3.png)

### Analisi Economico-Finanziaria

![](/assets/PowerBI/power2.png)

A questo punto possiamo continuare andando a fare un'analisi economico-finanziaria dei comuni, il kpi in alto mostra quanti di questi hanno dichiarato default tra il 2011 e il 2018.
Come prima, possiamo filtrare per località geografica oppure per reddito imponibile medio.
L'istogramma mostra 4 indicatori che in media differenziano i comuni deficitari da quelli sani 

![](/assets/PowerBI/power2.1.png)

Sotto abbiamo due misure fondamentali per il default possiamo visualizzarne i valori medi per comune o per provincia, i comuni deficitari sono colorati di rosso
Possiamo notare come i comuni deficitari siano in tutta italia, con prevalenza maggiore al sud

### Preprocessing
Il codice del preprocessing è disponibile qui **inserire link**, la sparsità dei dati di partenza non sempre ha permesso i join motivo per cui il dataset finale parte da 6000+ istanze anzichè tutti gli 8000 comuni italiani.

Inoltre, nel periodo di riferimento, un numero importante di comuni è stato soggetto a fusioni, rendendo impossibile il join.

Essendo fortemente sbilanciato il dataset abbiamo proceduto con un undersampling della classe maggioritaria
### Modello 

### Analisi Early-Warning

![](/assets/PowerBI/power3.png)

![](/assets/PowerBI/power3.2.png)

### Il team

Damiano Agachi Menna [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/damiano-am/)  
Simone De Bonis [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/SimoneDeBonis)  
Daniele Torregiani [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/daniele-torregiani-369b54243/)  
