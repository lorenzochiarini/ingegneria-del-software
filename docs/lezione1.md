indirizzo 137.204.107.21

# Ingegneria dei sistemi software

## Introduzione
Ingegneria dei sistemi software perchè vuole enfatizzare cose che non abbiamo ancora affrontato.  
Per risolvere un problema partiamo dai requisiti.  
Analisi dei requisiti molto importante.  
Sistema distrubuito ed eterogeno:

* **Distribuito**: presente su più nodi,
* **Eterogeneo**: scritto in più linguaggi.  

La domanda è quanto tempo ci metto e perchè.
Il laureato magistrale mi deve dire il tempo e il costo per un progetto.
Quindi devo saper organizzare per creare questo prodotto, facendo previsioni su quanto 
tempo mi ci vuole e quali tecnologie uso per la soluzione.
Ovvero parlo di _processo di produzione del **software**_.  
La demo è necessaria ma non sufficiente, per prendere il massimo devo mostrare il 
processo di produzione, ovvero mostrare il proggetto (perchè sono un ingegnere).  
Portare il progetto significa portare il modello delle classi (diagramma UML), ma non solo
infatti prima devo avere il risultato dell'analisi del problema, ma prima ancora l'analisi
dei requisiti.


> Il motto è non c'è codice senza progetto, ma non c'è progetto se prima non hai fatto 
> l'analisi del problema e il problema non sussiste se prima non ho fatto un'analisi dei requisiti.

La documentazione è una perdita di tempo.  
Il linguaggio naturare è un vincolo e perciò non va bene fare l'analisi dei requisiti 
con esso, perchè quello che diciamo potrebbe essere interpretato in modo diverso.
Quindi requisiti diversi, dato che li interpreto in modi diversi, datto soluzioni diversi.

Uso UML. L'Uml è insieme di standard, ma non siamo molto contenti di usarlo, perchè
definisce modelli per l'object oriented. Se voglio spiegare cos'è un'oggeto è meglio dire
è quello di Java, altrimenti in linguaggio naturale ognuno la pensa a modo sui.
Java è un linguaggio formale, cioè comprensibile alla macchina. Tutti i linguaggi di 
programmazione sono linguaggi formali. Anche Uml è un linguaggio formale, e usiamo un editor
per utilizzarlo e comprenderlo, perchè ci aiuta dandoci l'elenco dei simboli e ci 
corregge se li sbagliamo ad utilizzare.
Analisi dei requisiti in Uml sono i casi d'uso.
Cos'è la **Vision**?

> Ci ispira a fare quell'attività, 

Codice senza test è irrilevante.

I modelli dell'analisi dei requisiti e quello dell'analisi del problema sono correlati.
Se i requisiti sono uguali per tutti, allora anche le analisi di diverse persone devono 
essere uguali. Ottengo un documento uguale per tutti.

I requisiti che cambiano **l'architettura del sistema** sono quelli che mi danno più fastidio
se cambiano.

* **Architettura**:  
* **Sistema**: perchè fatto da più pezzi che interagiscono. Pezzi riusabili se compaioni in
più sistemi.

Nel modello ad oggetti, un oggetto passa il controllo ad un altro oggetto tramite procedure call
(schema di interazione), direi che non è molto buono como schema per sistemi distrubuiti.
Noi uomini interagiamo a scambio di messaggi.

* Fire and forget: lancio un messaggio poi non mi interessa se altri lo ricevono,
* Send and Response: chiedo e aspetto la risposta.

Noi vogliamo fare un **software factory**, costruisce il software come voglio io e con 
le tecnologie che dico io.
