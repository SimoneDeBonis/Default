---
title: Agenda Onu 2030
feature_text: 
feature_image: "https://simonedebonis.github.io/Projects/assets/Tableau/goals1.png"

excerpt: "A demo of Markdown and HTML includes"
aside: false
---

### Obiettivo
Gli [Obiettivi globali](https://www.globalgoals.org/) sono una serie di obiettivi molto ambiziosi proposti dalle nazioni unite, con lo scopo di preservare il pianeta e garantire un futuro più prospero per le generazioni future. Tra questi troviamo la povertà estrema, l'insicurezza alimentare, la disuguaglianza di genere, il cambiamento climatico e molto altro. Questi obiettivi sono interconnessi e si rafforzano reciprocamente, riconoscendo che la sostenibilità richiede un approccio olistico.

L’ambizione dell’Agenda si scontra con la difficoltà di misurare e tener traccia del raggiungimento o meno dei target definiti. Inoltre, è stato appurato che l’attuazione effettiva dell’Agenda sarebbe molto [costosa](https://www.reuters.com/business/sustainable-business/cost-hit-un-sustainability-goals-rises-176-trillion-report-2022-09-08/).

Questi obiettivi, noti anche come Obiettivi di Sviluppo Sostenibile (SDG), sono stati adottati nel 2015 e si propongono di essere raggiunti entro il 2030.

Dal momento che siamo a metà del periodo, a che punto è arrivata la sua attuazione?

Per poter confrontare lo stato degli indicatori al 2015 con gli ultimi dati disponibili, abbiamo sviluppato tre dashboard in Tableau, ognuna dedicata ad un Obiettivo specifico (Goal 8, Goal 9 e Goal 11).

### Dati
La fonte dei dati è [Our World in Data](https://sdg-tracker.org/), in cui sono raccolte le statistiche ufficiali ONU e delle altre organizzazioni nazionali e sovranazionali principali (ad esempio World Bank, OECD, IMF, ILO, …) collegate agli Indicatori individuati per l’Agenda 2030.

Nell’Agenda ogni Obiettivo/Goal ha dei propri Target, il cui raggiungimento viene verificato attraverso degli indicatori individuati dalle stesse Nazioni Unite come maggiormente idonei allo scopo. I dati disponibili si riferiscono agli indicatori. 

### Goal 8 - Lavoro Dignitoso e Crescita Economica

![](/assets/Tableau/goal8.png)
La mappa in alto a sinistra è dedicata al tasso di crescita del PIL per persona impiegata calcolato in media dal 2016 al 2021. Spiccano i paesi asiatici, i quali hanno registrato valori di crescita economica mediamente positivi dall’avvio dell’Agenda. Il dato medio italiano dal 2016 è pari a -0.2%, con tassi di crescita negativi già negli anni precedenti alla pandemia.

La visualizzazione in basso a sinistra presenta i valori di impronta materiale pro capite. In media una persona nel 2019 consumava annualmente 12,44 tonnellate di risorse per soddisfare la propria domanda di beni e servizi. Oltre ad esserci un trend evidente, il dato non sembra essere migliorato dal 2015.

Al centro, il grafico a dispersione mostra la dinamica nel tempo del PIL in relazione al Consumo Materiale Domestico pro capite. Diversi stati asiatici in crescita economica dal 2015 (ad esempio India, Turchia, Emirati Arabi, …) hanno aumentato al tempo stesso il proprio consumo interno di risorse per la produzione. Sintomo che, allo stato attuale, difficilmente è stato possibile migliorare la propria economia senza aumentare l’impatto della produzione sull’ambiente. 

L’ultimo grafico mostra il dato di NEET stimati per paese nel 2015 e nel 2019. L’Italia si colloca particolarmente in alto nella classifica, al quarto posto tra i paesi europei (21% nel 2015, 18% nel 2019).

### Goal 9 - Imprese, Innovazione e Infrastrutture

![](/assets/Tableau/goal9.png)
Il grafico a bolle permette in modo dinamico di visualizzare quanti sono i Kg di CO2 emessi da ogni paese per produrre un dollaro di PIL. E ancora una volta spiccano i paesi asiatici, con emissioni in media maggiori rispetto a quelle registrate negli altri continenti (0.327kg/$ nel 2018, rispetto ai 0.239kg/$ in media in Europa ed ai 0.251kg/$ in USA). L’Italia è tra i paesi più virtuosi, con un trend in calo negli ultimi decenni, e un dato di emissioni al di sotto delle media europea (0.168kg/$ nel 2018).

Per quanto riguardano gli investimenti in R&S, misurati con il numero di ricercatori ogni milione di abitanti, va sottolineata l’alta propensione alla ricerca nei paesi nordici (Danimarca in vetta con circa 8000 ricercatori ogni milione di abitanti nel 2018), di Sud Corea e Giappone, di Canada e USA. L’Italia è in 36° posizione, contando circa 2300 ricercatori per milione di abitanti nel 2018. Agire sugli investimenti in questo settore è fondamentale per stimolare la produttività e la crescita economica dei singoli paesi.

Infine, l’ultima tabella a destra mostra i valori di accesso ad Internet nel 2015 e 2020, per visualizzare i paesi che tutt’ora non riescono a garantire una copertura universale alla popolazione.

### Goal 11 - Città e Comunità Sostenibili

![](/assets/Tableau/goal11.png)
La tabella a sinistra contiene le percentuali delle persone che vivono in abitazioni anguste, senza acqua potabile o servizi igienici, o in edifici instabili. Considerando i dati dal 2014 al 2018, i Paesi in peggioramento sono la Siria (dal 19,3% al 37,9%) e la Giordania (dal 12,9% al 23,4%), il Myanmar (dal 41% al 56,1%), il Venezuela (da 32% a 44,1%) e la Colombia (da 13,1% a 27,8%). 

La mappa in alto a destra indica quali sono i paesi ad aver subito maggiori danni vitali ed economici per i disastri naturali. La Francia registra un dato molto elevato di decessi legati alle intense ondate di calore nel periodo estivo. Gli USA invece, nonostante i bassi valori di mortalità, hanno speso in media 90 miliardi di dollari all’anno dal 2016 al 2021 per i danni legati agli uragani e ad altri disastri naturali.

L’ultima visualizzazione confronta i valori di esposizione media di PM2.5 di ogni paese dal 2015 al 2017. 
La situazione è critica nella penisola arabica, in altri stati asiatici (come l’India) e africani (come l’Egitto): i paesi con reddito pro capite più basso hanno esposizioni molto elevate a causa dell’utilizzo prevalente di fonti energetiche non rinnovabili e di impianti produttivi altamente inquinanti.



### Il team

 
Damiano Agachi Menna [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/damiano-am/)  
Simone De Bonis [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/SimoneDeBonis)  
Daniele Torregiani [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/daniele-torregiani-369b54243/)  
