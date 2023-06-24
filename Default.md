---
title: Early Warning dei default dei comuni italiani
feature_text: 
feature_image: "https://simonedebonis.github.io/Projects/assets/artificial-intelligence.jpg"
excerpt: "A demo of Markdown and HTML includes"
aside: false
---

# Analisi
Il “default”, meglio definito come “dissesto finanziario” si verifica quando un comune caratterizzato da gravi ed incontrovertibili condizioni di squilibrio finanziario non riesce più a svolgere le sue funzioni di base e a fornire alla cittadinanza quei servizi considerati indispensabili. 
Il dissesto è una cosa ben diversa dal fallimento di un’impresa privata: non si può determinare l’estinzione del comune proprio perché́ gli enti locali non possono cessare di esistere, ma bisogna garantire la continuità̀ amministrativa. 
Il dissesto di un comune è una procedura complessa che impatta negativamente sulla qualità della vita dei suoi cittadini. Comprendere perché questo succeda è fondamentale per prevenirlo agendo tempestivamente. L’analisi si concentra sull’anno 2018.

Partendo da Open Data italiani provenienti dal Ministero dell’Interno, OpenCivitas, Ministero delle Finanze e ISTAT abbiamo costruito il dataset in modo multidimensionale, incorporando sia gli aspetti sociali che finanziari. 
Le variabili sociali includono il genere, l’età e l’istruzione del sindaco, il numero di abitanti medi nel periodo 2012-2018. L’utilizzo a fini di analisi del partito politico di appartenenza del sindaco è limitato dalla presenza massiccia di liste civiche non riconducibili alle aree politiche di appartenenza.
Le variabili finanziarie includono Fondo Perequativo, Fondo Storico, Rimborso prestiti su entrate correnti, Rigidità della spesa, Reddito imponibile individuale, Consistenza iniziale dei residui passivi, Popolazione media, Spese personale su spese correnti, Grado di finanziamento interno, Dipendenza da finanziamento esterno, Dipendenza da contributi e trasferimenti correnti ed Autonomia impositiva.
In aggiunta è stato sviluppato un modello di Early Warning, un SVM con kernel radiale, per prevedere futuri default. Non essendo presenti dati aggiornati e visti i problemi derivanti dalla pandemia, nella dashboard sono considerati Early Warning le misclassificazioni del modello: un comune sano predetto in default dall’svm viene considerato come tale.
### Il team

 
Damiano Agachi Menna [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/damiano-am/)  
Simone De Bonis [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/SimoneDeBonis)  
Daniele Torregiani [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/daniele-torregiani-369b54243/)  
