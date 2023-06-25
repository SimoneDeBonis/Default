---
title: Analisi del mix Energetico dei paesi europei
feature_text: 
feature_image: "https://simonedebonis.github.io/Projects/assets/artificial-intelligence.jpg"
excerpt: "A demo of Markdown and HTML includes"
aside: false
---

# Obiettivo
- Visualizzare il mix di produzione elettrica dei Paesi Europei 
- Analisi degli scambi comunitari
- Impatto ambientale del settore energetico

# Dati Eurostat e JRC
- Produzione interna sulla base delle fonti impiegate
- Import ed export
- Sociali-economici
- Emissioni del settore energy
- Impatto delle diossine sulla salute pubblica
- Posizione geografica delle centrali elettriche
- Performance e emissioni dei siti produttivi

# Mix Energetico
### Mix Energetico Italia 2022
![](/assets/Qlik/Dashboard1.png)
La dashboard 'Mix Energetico' è uno strumento completo che consente di analizzare in dettaglio la produzione interna di energia di ciascun paese europeo, fornendo risposte a quesiti del tipo:  quando e quali sorgenti di energia la nazione X ha impiegato nell'anno XXXX? Grazie alla presenza di due pulsanti di navigazione indicati con i nomi delle rispettive sezioni, l'esplorazione e la navigazione all'interno della dashboard é intuitive e semplici.

### KPI
All'interno della dashboard, la parte superiore ospita un KPI multiplo che riporta il valore medio europeo delle sei principali fonti di energia: 'Fossile', 'Nucleare', 'Geotermico', 'Solare', 'Eolico' e 'Idroelettrico'. Questo indicatore permette di avere una visione globale e confrontabile del panorama energetico europeo. Inoltre, considerando il nucleare come fonte 'Verde', l'indicatore successivo fornisce una stima della quantità di energia prodotta dalle sorgenti fossili e da quelle verdi, offrendo così un'immagine complessiva della qualità del sistema produttivo della nazione selezionata.

Gli ultimi due KPI presenti nella dashboard forniscono informazioni su: il primo indica la quantità media di energia consumata da un cittadino in un anno, offrendo un'indicazione chiara dei livelli di consumo energetico della popolazione; il secondo KPI rappresenta la percentuale di energia verde consumata da un cittadino. Consentendo un confronto diretto con altri paesi europei e la possibilità di valutare se la nazione in esame si posizioni tra i paesi più virtuosi o meno in termini di consumo di energia verde.
Questi KPI sono essenziali per valutare l'efficacia delle politiche energetiche di ciascun paese, per avere una fotogragia della situazioen attuale ed individuare una strategia per incrementare la produzione di enegrgia elettrica da fonti verdi.

### Fonti impiegate
Il grafico a ciambella mostra le principali fonti di energia utilizzate per la produzione di elettricità in Italia nell'anno 2022. Come era prevedibile, la fonte fossile più diffusa è il gas naturale, seguito da fonti di energia verde e da altre fonti inquinanti che coprono una percentuale significativa della produzione nazionale. Questo grafico permette di comprendere immediatamente la composizione del mix energetico italiano e di identificare le fonti che richiedono una maggiore attenzione in termini di riduzione delle emissioni.

### Mix energetico
Un altro strumento di visualizzazione fornito dalla dashboard è il grafico a linee, che riporta la produzione mensile delle sei fonti di energia nel periodo 2016-2022. Questo tipo di visualizzazione è estremamente utile per analizzare l'andamento nel medio periodo e comprendere l'andamento di produzione delle diverse fonti di energia. In particolare, si può notare la presenza di una stagionalità dovuta ai consumi e alla produzione di alcune categorie di energia. Ad esempio, il grafico evidenzia l'aumento significativo dell'energia solare e idroelettrica durante l'estate, l'energia eolica che registra un aumento di produzione durante la primavera e l'autunno, e la costanza dell'energia geotermica nel corso di tutto l'anno.

### Mix Energetico Germania 2022
![](/assets/Qlik/Dashboard1.2.png)
Nello stesso periodo, in Germania, il consumo pro capite è stato di 6,19 MWh, registrando una diminuzione dell'11,5% rispetto al 2016 e del 10% rispetto al periodo pre-Covid. Tuttavia, la Germania detiene il primato del consumo individuale più elevato in tutto il vecchio continente. Nel 2022, il 46,95% dei consumi tedeschi è stato prodotto da fonti "Verdi", evidenziando una crescita del 14,72% negli ultimi 7 anni. Nonostante ciò, tale percentuale è inferiore al picco massimo raggiunto nel 2020, quando ha raggiunto il 50,58%. Ciò indica che la Germania si avvicina di più alla media europea rispetto all'Italia in termini di consumo di energia da fonti verdi.

Le fonti verdi, come l'eolico e il solare, hanno avuto un peso maggiore nel sistema produttivo tedesco rispetto alle medie europee, nonostante l'uso ancora intenso di materiali altamente inquinanti come il carbone e il gas. Dal punto di vista temporale, la sorgente "Fossili" è sempre meno utilizzata (ad eccezione dell'anno 2022) e viene sostituita da fonti "Verdi" come l'eolico e il solare. Allo stesso tempo, l'energia nucleare sta perdendo importanza nel portafoglio produttivo tedesco poiché le poche centrali ancora in funzione sono in fase di dismissione.

### Top Paesi per produzione elettrica sulla base della fonte

Passando alla sezione "Top Paesi per produzione elettrica sulla base della fonte" all'interno della dashboard, è possibile utilizzare il filtro 'Fonte' posizionato sul lato sinistro per selezionare la categoria desiderata e ottenere una classifica dei paesi europei che maggiormente sfruttano quella specifica fonte nel proprio piano di produzione energetica nazionale. Ad esempio, impostando il filtro su 'Fossili', si nota che la Germania è il paese europeo che maggiormente fa uso di questa fonte in termini assoluti, seguita dall'Italia e dalla Turchia. Tuttavia, è la Polonia il paese europeo che si affida maggiormente alle fonti non rinnovabili per generare la propria corrente elettrica.


In conclusione, la dashboard 'Mix Energetico' attraverso visualizzazioni efficaci permette di comprendere i dati della produzione di energia elettrica in modo dettagliato, offre una panoramica completa dei mix energetici dei paesi europei e la possibilità di confrontarli tra essi. 

# Analisi commerciale

![](/assets/Qlik/Dashboard2.png)
Attraverso il pulsante 'Analisi', è possibile accedere alla seconda dashboard che si focalizza sull'analisi commerciale dell'energia, fornendo anche alcuni insights riguardanti gli aspetti socio-economici del paese selezionato.

### KPI
I KPI presenti nella parte superiore della dashboard mostrano la variazione annuale delle importazioni e delle esportazioni di energia elettrica e la loro percentuale rispetto alla produzione totale del paese selezionato. Questo può essere utilizzato come un indicatore per valutare l'indipendenza dalle forniture estere. Prendendo ad esempio l'Italia nel 2021, si osserva un aumento delle importazioni di energia, diventando un importatore netto di 43 TWh dai paesi confinanti. Inoltre, dal 2016 la dipendenza energetica dall'estero è aumentata del 15,56%, peggiorando il saldo energetico annuale e quello a medio termine fissato a 5 anni.

### Aspetti socio-economici
Nel corso degli anni, il divario di genere nel mercato del lavoro italiano ha mostrato una situazione pressoché stabile. Si è passati dal rapporto occupazionale maschile-femminile del 57,9% - 42,1% nel 2016 al 57,6% - 42,4% nel 2021.
Nel periodo tra il 2011 e il 2015, il costo dell'elettricità per uso domestico è aumentato del 25%, mentre il PIL pro capite nello stesso periodo è diminuito del 4,3%. Ciò rende il costo dell'energia sempre più rilevante nel bilancio delle famiglie italiane. Durante l'ultimo periodo di pandemia, i due indicatori hanno mostrato un andamento simile.

### Importazioni ed esportazioni
Sul lato sinistro della dashboard sono presenti due grafici che tracciano le importazioni ed esportazioni del paese Italia. È possibile notare che i partner più rilevanti in entrambe le direzioni del flusso energetico sono la Svizzera e la Francia. Nonostante le esportazioni italiane rappresentino solo l'1,36% del fabbisogno totale, ci sono scambi in uscita verso le nazioni citate in precedenza a causa della difficoltà di prevedere il consumo energetico nel corso del tempo e della limitata flessibilità della produzione nel adattarsi rapidamente alla domanda. Pertanto, quando si verifica un eccesso di produzione da parte di un paese e una mancanza di offerta da parte dell'altro, avvengono tali scambi che solitamente avvengono in direzioni invertite.

![](/assets/Qlik/dashboard2.2.png)
Nel corso del 2021, la Francia ha mantenuto una bilancia commerciale positiva di 45 TWh, confermando il suo ruolo di maggior esportatore di energia elettrica nel continente. Questo valore è aumentato dell'8,17% rispetto agli ultimi 5 anni. Tra i principali partner verso cui la Francia esporta energia, troviamo l'Italia, il Regno Unito, il Belgio e la Spagna. Un aspetto interessante è che l'Italia appare tra i paesi da cui la Francia importa energia, principalmente a causa del fatto che la Corsica soddisfa il suo fabbisogno energetico attraverso l'esportazione italiana.

Analizzando l'occupazione femminile in Francia, si può osservare un aumento dal 48,35% nel 2016 al 48,96% nel 2021. Questo indica una disparità occupazionale inferiore rispetto all'Italia. Ampliando l'analisi ai paesi nordici, emerge una caratteristica comune: una bassa disparità occupazionale tra generi e un maggiore utilizzo delle fonti di energia rinnovabile rispetto all'Italia o ad altri paesi con caratteristiche simili. Questo tipo di confronto é ancora più accentuato nel confronto tra i paesi scandinavi e la Polonia o la Bulgaria.

Passando all'analisi economica, nel periodo tra il 2011 e il 2021, il costo dell'elettricità per le utenze domestiche in Francia è aumentato del 35,7%. Nel frattempo, il PIL pro capite è cresciuto solo del 4,2%. Come già evidenziato per l'Italia, anche per i cittadini francesi il costo dell'elettricità è diventato sempre più rilevante nel corso degli anni, sebbene il costo per kWh sia inferiore rispetto all'Italia (0,2 €/kWh rispetto a 0,23 €/kWh). Per le utenze industriali, i prezzi sono rimasti pressoché stabili fino al 2021, sebbene vi siano differenze di prezzo tra i due paesi.

In conclusione, questa dashboard fornisce una prospettiva approfondita sull'aspetto commerciale e socio-economico dell'energia elettrica, consentendo di valutare la dipendenza dalle forniture estere, il divario di genere nel mercato del lavoro e l'impatto dei costi energetici sui cittadini. Tali informazioni sono di fondamentale importanza per l'analisi strategica e la pianificazione delle politiche energetiche ed individuare le caratteristiche che determinano il sistema paese.

# Impatto ambientale

![](/assets/Qlik/Dashboard3.png)
Nella terza dashboard, troviamo visualizzazioni che mettono in evidenza l'efficienza delle reti produttive nazionali e l'impatto delle emissioni sulla salute dei cittadini.
### KPI
I KPI in alto forniscono informazioni sulle quantità di CO2 emesse dalle centrali elettriche, la loro efficienza media e i danni in termini di vite umane causati dalle diossine rilasciate. In Italia, l'impatto del settore energetico sull'ambiente è in diminuzione, con le emissioni che si attestano al 31% nel 2020, al di sotto della media europea stabile al 34% delle emissioni totali. Si stima che nel 2017, i giorni di vita persi pro capite a causa dell'esposizione a diossine come i PM10 e PM2.5 fossero di 3,23 giorni, riducendosi a 2,83 giorni nel 2020, pur rimanendo superiori alla media europea di 2,1 giorni, mentre i morti precoci dovuti a problemi respiratori e/o cardiaci che sono causati dallo smog si stimano essere circa 50 mila all'anno.

Il grafico composto rappresenta l'andamento dell'indice di decarbonizzazione, con un valore di riferimento pari a 100 nel 2000, che indica quanto un paese abbia ridotto la propria impronta di CO2 nel corso degli anni. Anche in questa situazione, l'Italia é in linea con i partner europei.

Inoltre, è possibile osservare la quantità di kg di CO2 emessa per produrre un MWh dalle diverse tipologie di centrali. Nel caso dell'Italia, le centrali a gas, essendo anche le più diffuse, sono quelle che, in termini assoluti, inquinano di più.
### Mappa
Successivamente, è possibile visualizzare le centrali sul territorio selezionato, identificando facilmente la loro tipologia in base al colore e la loro rilevanza in base alla grandezza del punto localizzatore. Passando con il cursore sopra di esse, è possibile ottenere maggiori informazioni tecniche. Vi é la possibilità di avere un'anteprima del mix energetico dei paesi europei, passando sopra la torta sovrapposta a ciascuno di essi e scoprire in quale percentuali ciascuna fonte é stata impiegata nello specifico anno per generare elettricità.
![](/assets/Qlik/Dashboard3.2.png)
![](/assets/Qlik/Dashboard3.3.png)
Nonostante la forte dipendenza dalle fonti fossili, in particolare dal gas, carbone e petrolio, e data la buona efficienza media degli impianti di generazione elettrica, l'Italia si mantiene in linea con gli altri Paesi europei nella riduzione degli inquinanti atmosferici del settore energy. 

### Il team

 
Damiano Agachi Menna [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/damiano-am/)  
Simone De Bonis [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/SimoneDeBonis)  
Daniele Torregiani [{% include icon.html id="linkedin" title="twitter" %}](https://www.linkedin.com/in/daniele-torregiani-369b54243/)  
