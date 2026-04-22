# Homework 1 per Linguaggi per il Web - XHTML e CSS

## Autore: Lorenzo Petrucci

## Repository di GitHub:
[LinguaggiWeb-XHTML_CSS su GitHub](https://github.com/lorenzopetrucci1937262/LinguaggiWeb-XHTML_CSS)

## Funzione del sito
Il sito ha lo scopo di simulare la presenza web di un cinema multisala. 
Viene offerta all'utente una vetrina dei film in sala, una presentazione di quello che
un cliente può chiedersi riguardo al cinema ed un calendario delle principali uscite in sala 
nei prossimi mesi. 

## Funzionalità del sito
Il sito presenta la navigazione tra pagine tramite i link nell'header, e la navigazione all'interno 
della stessa pagina nella pagina della programmazione con link ad id dei film in calendario. 
I film in calendario gia presenti in sala sono raggiungibili anche da titolo e immagine delle loro 
anteprime nella home. Infine per ogni film c'è il link al trailer su youtube. 

## Struttura del sito
### HOME
La pagina principale rappresenta la vetrina del cinema, come per strada, l'occhio viene rapito 
da i cartelloni dei film in proiezione. La struttura è classica con header e footer, al centro 
si presenta la vetrina come 3 colonne con distanze fisse. Ogni colonna vuole rappresentare il 
cartellone del film per cui sotto il poster ci sono i dettagli salienti. 
La home rappresenta il punto di partenza del sito, dando la possibilità all'utente di navigare 
per andare alle altre due pagine dailink nell'header e di arrivare alle schede complete sui film 
in sala dall'immagine o dal titolo presenti in vetrina.

### PRESENTAZIONE
La pagina presentazione rappresenta un biglietto da visita espanso del cinema, completa di tutte, o quasi, 
le risposte alle possibili domande del cliente. Ci sono in ordine le informazioni sulle sale di proiezione, 
le informazioni sui prezzi e sugli abbonamenti. Queste informazioni sono disposte in tre sezioni separate ma 
strutturalmente simili. Questa è una pagina esclusivamente informativa per cui si è prestata all'esercizio 
sull'uso delle tabelle. La staticità della pagina trova riscontro nel fatto che il suo contenuto è l'unico 
nel sito che si scaglia sullo sfondo senza un appoggio visivo come per le altre pagine in cui i contenuti sono 
ben incasellati. L'idea è quella di mettersi a nudo, come se questo contenuto facesse da sfondo a tutto il sito 
se si potessee vedere sotto i div chissà... 

### PROGRAMMAZIONE
La pagina programmazione è quel mini giornaletto, quel depliant con gli eventi, o film, futuri o in programma.
L'importanza di dare al cliente le informazioni che lo porteranno poi in sala è riportata tutta in questa pagina. 
Ogni film in uscita in una scheda esaustiva con tutte le informazioni ufficiali sul film, con tanto di immagine notevolmente ingrandita rispetto all'anteprima nella home. A completare il quadro una sidebar di navigazione 
'appiccicata' sulla destra della pagina. La sidebar rappresenta il modo più rapido di leggere il calendario completo, 
evitando di scrollare, e di raggiungere il film d'interesse con il link all'id del film. A completare la barra le informazioni sugli spettacoli. 

## NOTE DI SVILUPPO
### SIDEBAR
Vari tentativi sono stati necessari per capire il metodo più efficiente e anche visivamente adatto per fare in modo 
che la sidebar fosse fissa a schermo durante lo scroll. Si è provato con :fixed, con degli anchor e a fissare anche header, Mostruosità aberranti. Alla fine con sticky è uscita una soluzione elegante insperata visto che all'inizio 
non era stato preso molto in considerazione.

### HEADER
Non è stato un colpo di fulmine ma ci sono voluti più e più tiri in porta per fare alla fine goal. Non c'era verso di 
incastrare due link ai lati e il titolo al centro in modo accettabile. L'idea alla fine era di mettere una barra di navigazione subito sotto al titolo... terrificante. Ma non tutto il male vien per nuocere, tant'è che per fare questa 
barra uso display: flex con justify-content: space-between e ho visto la luce. Rifatto nell'header e tutto a posto.

### ANTEPRIMA FILM HOME
La soluzione meno bella e il tallone d'achille è la gestione dell'altezza delle anteprime dei film nella home. Sono costruite per allungarsi con il testo per cui finivano per avere altezze diverse. Visivamente brutto, i tentativi di avvicinarli hanno avuto risultati mediocri. L'unica cosa che si è avvicinata era min-height ma ce n'era sempre uno che la superava e finiva per rompere il footer spostandolo. La soluzione finale è stata height fissa. Con upgrade si punta anche a sistemare.