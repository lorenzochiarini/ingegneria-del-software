## Laboratorio 1 - Strumenti
[Laboratorio 1 - letture](https://137.204.107.21/syskb/it.unibo.iss2015intro/docs/Lab/Lab2016/Starting2016.html)

Un problema che va affrontato è l'automatizzazione dei processi. Gradle permette di accellerare la velocità dello sviluppatore.  
L'idea è che noi abbiamo una commessa, e che quindi non siamo noi a dare i requisiti.  
I requisiti si dividono in:

* **Funzionali**: il problema deve fare certe cose,
* **Non fonuzionali**: il software deve avere certe caratteristiche (modularità, estendibilità ecc.).  

The main goal is understand both what should be done in a software development process and how do it, with the help of tools and modern frameworks or run-time platforms (general purpose and/or custom).

Per superare l'esame, prof da un requisito noi lo capiamo facciamo delle cose e dimostriamo che funziona come se il prof fosse il committente. Sviluppare codice e dire come è stato fatto al prof, quindi spiegare i motivi di certe scelte.

Progetto:
* Analisi dei requisiti,
* Analisi del problema,
* Progettazione.

Avremo dei requisiti su sistemi software distrubuiti ed eterogenei. In ogni caso si inzia sempre creandolo contentrato, quindi nel processo iniziale crearemo un progetto non distrubuito.

 
> L'idea prevale sul progetto.

Come portare l'analisi dei requisiti? La _visione_ dice che non deve essere un foglio word, ma che già ci sia un prototipo del sistema, qualche cosa che possa mostrare al committente in modo che lo possa valutare. Si chiama **Prototipo**, ma ancora meglio possiamo dire la parola ingegnericamente migliore, abbiamo un **MODELLO**.

> Il Modello è una rappresentazione semplificata del sistema che cattura gli  aspetti essenziali. 

Esempio ho come requisito che se premo button si accende il led, ripremo il button e spengo il led. Il modello è composto da due elementi.
Non abbiamo nessun vincolo, ma vogliamo un prototipo concentrato, ovvero non distrubuito.
Noi non possiamo inziare fino a quando il committente non ci spiega come sono il led e il bottone, sono fisici oppure no.

La classe è una rappresentazione che esprime le proprietà importanti dell'entità che vogliamo modellare.

Devo fare un sistema fatto da due elementi button e led, l'idea è che quando premo il button si deve accendere il led e se ripremo si deve spegnere. L'azione è la stessa ma una volta succede una cosa e l'altra volta un'altra.
Nell'analisi dei requisiti cercate di capire cosa sia per il committente un button e il led, e cosa significa premere un button. Facendo risposte al committente posso fare la rappresentazione del sistema in java, ma non la soluzione.

Il computer lavora esclusivamente sulle rappresentazioni.
La differenza fra paradigma OO e paradigma funzionale è che lo stato non cambia mai.

Il button è l'istanza di un dispositivo di input (sorgente di informazione che io devo elaborare), il led invece è l'output. Il terzo componente è quello che esegue l'elaborazione.
Quindi sistemi sempre composti da:

* Input,
* Output, 
* Elaborazione.

Input invia info all'elaborazione e lui all'output. Non ho mai interazione diretta fra input e output. Modello di qualunque applicazione informatica.

L'output è più facile, mentre l'input è un casino. Perchè l'output decide lui cosa fare, mentre l'input dipende da quale interazione fa.

Interfaccia dice cosa fai(esprime un contratto), ma non il come e in fase di analisi dei requisiti è più importante il cosa.

Mercoledì devvo portare un esempio di una rappresentazione più generale caratteristica di tutte le applicazioni in cui riconosco un input, un output e un'elaborazione, il button input led output e io devo fare l'elaborazione.
Led dispositivo di output in grado di emettere luce.

```
public Interface ILed {

    public void turnOn(); // mi accendo.
    public void turnOff(); // mi spengo.
    public boolean isOn(); // true acceso, false spento.
}
```

Il commento è fuffa, quindi devo fare dei test. Pianifichiamo i test: 
* Primo test: `led.isOn()` vediamo lo stato, e dobbiamo fare in modo che sia spento `false`.
* Secondo: accendo `led.turnOn()`, poi faccio `led.isOn()` e mi aspetto `true`

JUnit per fare i test, perchè non voglio fare i test a mano, ma automatizzati.

Non mi può cambiare l'architettura logica del sistema, ma quella implementativa si, magari fatto con arduino, oppure virtuale.

## X Mercoledì

`it.unibo.bls0` nome del progetto
per ogni classe scriviamo questa non è una classe di implementazione, ma classe di requisito.

[ButtonLed](https://137.204.107.21/syskb/it.unibo.iss2015intro/docs/Appls/ButtonLed/buttonLed.html)

Il bottone è un'entità autonoma che cambia stato, e io devo accorgermi di questo cambiamento, perchè non è sotto il controllo del sistema.