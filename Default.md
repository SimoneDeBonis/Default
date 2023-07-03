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

### Preprocessing
Il codice del preprocessing è disponibile [qui](), la sparsità dei dati di partenza non sempre ha permesso i join motivo per cui il dataset finale parte da 6000+ istanze anzichè tutti gli 8000 comuni italiani.

Inoltre, nel periodo di riferimento, un numero importante di comuni è stato soggetto a fusioni, rendendo impossibile il join.
### Il team

 
Damiano Agachi Menna [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/damiano-am/)  
Simone De Bonis [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/SimoneDeBonis)  
Daniele Torregiani [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/daniele-torregiani-369b54243/)  
