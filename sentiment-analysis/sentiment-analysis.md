# Sentiment Analysis

Abbiamo iniziato questo libro parlando di interpretazione a livello micro: una lettura attenta chiede di prestare attenzione a ogni piccolo dettaglio di un testo per produrre analisi. Poi abbiamo fatto uno zoom su cosa potremmo ottenere dalla lettura a livello  macro e come i computer ci consentono di comprendere i testi in modi nuovi. Ora, nella fase finale, ritorniamo all'inizio.

Più volte è stata sottolineata l'interazione tra calcolo e interpretazione: quando il computer ti presenta dei risultati, il tuo lavoro è appena iniziato. Il computer può fornire dati, ma sei tu che devi interpretarli. Il computer di fatto non legge. Tu lo fai. E, dunque,  ciò che hai imparato è come leggere con i computer.&#x20;

Ma probabilmente hai anche notato negli ultimi capitoli che i tipi di letture per cui utilizziamo i nostri computer sono diventati più sofisticati. Quando utilizziamo un software per scoprire gli argomenti di cui un testo sta discutendo o per identificare autori anonimi, non li stiamo facendo leggere come farebbe una persona. Ma ci stiamo avvicinando a come un essere umano legge. Queste tecniche mirano, infatti, a fornire un senso più ricco di un testo e lo fanno in modi appunto piuttosto sofisticati. Chiudiamo iul nostro percorso con un problema un po' più semplice, ma di fatto profondamente difficile per i computer: un particolare testo è felice o triste? Per esserlo, ciò che conta è una frase? O è una parola?

L' analisi che cerca di catturare la risonanza emotiva di un testo è chiamata **sentiment analysis**. **** Probabilmente, ne hai fatto esperienza senza rendertene conto. Se sei mai stato in un sito di recensioni come [Rotten Tomatoes](https://www.rottentomatoes.com/) per vedere quale punteggio un film abbia ottentuto, stai guardando un numero aggregato di recensioni che sono state contrassegnate come positive o negative.

![](../.gitbook/assets/screenshot-www.rottentomatoes.com-2022.05.31-12\_07\_57.png)

Anche le aziende hanno un interesse in queste cose. Se fai un tweet su un tuo volo recente, la compagnia aerea probabilmente vorrebbe sapere se l'hai apprezzata o meno. Nel primo potresti essere indirizzato al servizio clienti, mentre nel secondo potrebbe ricevere una risposta come "grazie per aver volato con noi!".



La sentiment analysis può anche offrire interessanti opportunità per l'analisi testuale. Dai un'occhiata a questa clip di una conferenza di [Kurt Vonnegut](https://it.wikipedia.org/wiki/Kurt\_Vonnegut). La comunicazione è comico/sarcastico/satirica (decidi tu); se non conosci l'inglese imposta la traduzione automatica.

{% embed url="https://www.youtube.com/watch?t=26s&v=oP3c1h8v2ZQ" %}

{% hint style="info" %}
[Qui ](https://www.personalreport.it/2012/01/la-forma-delle-storie-per-kurt-vonnegut/)una spiegazione dei contenuti del video.

La questione della forma delle storie è piuttosto interessante. Qui trovi una eccellente trattazione dell'argomento [Ups and Downs. Or how to graph a book.](https://www.laphamsquarterly.org/roundtable/ups-and-downs) &#x20;

Nel 2016 i membri del [Computational Story Lab dell'Università del Vermont](https://compstorylab.org/) hanno quantificato le "complesse traiettorie emotive" di 1.327 opere classiche tracciando la frequenza delle parole classificate come felici (incluse _gioia_ , _amore_ e _pace_) o infelici (inclusi _odio_, _vergogna_ e _morte_). I risultati del cosiddetto [edonometro ](https://hedonometer.org/books/v1/?lens=\[3,5.25])dei ricercatori mostrano l'aumento e la diminuzione relativi delle emozioni positive e negative nei libri disponibili sul [Progetto Gutenberg](https://www.gutenberg.org/).&#x20;

Il team del Computational Story Lab, che ha anche quantificato la felicità su Twitter, nelle notizie e altrove, ha trovato ispirazione nella teoria della forma delle storie di [Kurt Vonnegut](https://www.laphamsquarterly.org/contributors/vonnegut). Vonnegut ha affermato che le storie hanno forme semplici che tracciano l'arco della relativa buona o cattiva fortuna dei loro protagonisti, una teoria che ha condiviso nel video visto sopra e  per [iscritto](https://www.laphamsquarterly.org/arts-letters/blackboard).


{% endhint %}

L'idea ha abbastanza senso per come la presenta Vonnegut: in determinati momenti in una storia, le cose sono di vario grado, buone o cattive. Come con qualsiasi forma di analisi del testo, questo tipo di informazioni potrebbe essere molto utile per la comprensione di un testo.

* Che tipo di emozioni impiega l'autore nel testo? Quando?&#x20;
* In che modo le emozioni si associano ad altre categorie estetiche, come la struttura narrativa?&#x20;

Sarebbe affascinante avere un computer in grado di individuare facilmente i sentimenti nei testi per te. Tuttavia, se finora hai seguito con attenzione, dovresti sapere che i computer non possono fare molto senza che venga loro detto esplicitamente cosa e come fare. Possono fare molto poco in termini di comprensione dei dati senza un essere umano che li guidi. Cercare di estrarre informazioni complicate come la traiettoria sentimentale di un testo, come dovremmo sentirci riguardo a una frase o come un autore intendeva farci sentire, sono tutti compiti complicati con cui i computer hanno difficoltà. E, in effetti, pure due persone diverse potrebbere avere difficoltà a mettersi d'accordo. Prova a indovinare se queste due frasi sarebbero classificate come positive o negative:

* "I am very happy." (Io sono molto felice)
* "She is so sad." (Lei è così triste)

Erano esempi facili, come _caldo_ e _freddo_. Che ne dici di questo?

* “It was the best of times, it was the worst of times…” (E' stato il migliore dei rempi, è stato il peggiore dei tempi...)

Questa frase è tratta dal racconto _Tale of Two Cities_ di Charles Dickens ed è probabilmente un po' difficile da analizzare in modo binario. Se è sia buono che cattivo; probabilmente risulta neutro, giusto? Ma qui Dickens parlava dell'era della Rivoluzione francese; intendeva che si era trattato di un momento straordinario, una situazione difficilmente "neutrale". In effetti, è interessato a giustapporre cose diverse - best/worst, London/Paris, ecc. - non ha risolverle. Avremmo probabilmente bisogno di un sistema per determinare cosa fare in tali situazioni.&#x20;

Osserva ora questa frase di Jane Austen, che complica ulteriormente le cose:

"It is a truth universally acknowledged, that a single man in possession of a good fortune, must be in want of a wife." ("È una verità universalmente riconosciuta, che un uomo single in possesso di una buona fortuna, deve essere alla ricerca di una moglie.")

Un'appassionata lettrice di Austen saprebbe che i suoi testi sono carichi di satira. È improbabile che la Austen si aspetti davvero che le sue parole siano prese alla lettera:  quindi la frase strizza l'occhio al lettore e non dovrebbe essere presa sul serio. In effetti, gran parte del suo lavoro è inteso come una critica feroce alla cultura e alle persone che la circondano, realizzata in gran parte in modo indiretto, espressa con ironia e satira che chiedono al lettore di leggere contro ciò che il testo apparentemenete afferma.&#x20;

Tutte queste _nuances_ sono difficili da trasmettere ai lettori, per non parlare dei computer. Dunque, la sentiment analysis attraverso la tecnologia è complicata, ma ciò non significa che i ricercatori non ci provino. Il processo è difficile e pieno di errori, ma anche intellettualmente interessante in diversi modi.

* Come possiamo mappare idee astratte e complicate come le emozioni in un modo che i computer possano capirle?
* Cosa può dirci una sentiment anaòysis come questa sugli oggetti che studiamo?

Come con qualsiasi forma di analisi del testo, i potenziali usi spaziano tanto quanto la nostra immaginazione. Un convincente esempio d'uso della sentiment analysis è offerto da [David Robinson ](http://varianceexplained.org/r/trump-tweets/)che ha cercato di misurare il grado di controllo che la campagna di Donald Trump aveva sul suo account Twitter. Sapendo che Trump tendeva a utilizzare un Samsung Galaxy per twittare, Robinson voleva determinare se i tweet di diverse tecnologie potessero avere caratteristiche diverse. In questo caso, si sarebbe ragionevolmente potuto separare la sua _persona personale_ su Twitter da quella curata dalla sua campagna. Robinson ha scoperto che potevamo ragionevolmente determinare che i tweet più arrabbiati e iperbolici provenissero da un Samsung Galaxy (ed era più probabile che provenissero dallo stesso Trump). È più probabile che i tweet degli iPhone fossero "dichiarazioni abbastanza positive". Su questa base ha distinto i gestori della campagna di Trump da Trump stesso.

Computers might not be able to feel, but perhaps we can train them to know what emotions look like. The very idea of measuring sentiment computationally is provocative. If we were working in big business, we would care a lot about the results of such projects. But, as humanists, we can also gain a lot just from trying to model such complicated topics. The process is as enlightening as the product.

I computer potrebbero non essere in grado di sentire, ma forse possiamo addestrarli a sapere che aspetto hanno le emozioni. E l'idea stessa di misurare il sentimento in modo computazionale è provocatoria. Se lavorassimo in una grande impresa, ci preoccuperemmo molto dei risultati di tali progetti. Ma, come umanisti, possiamo anche ottenere molto solo cercando di modellare argomenti così complicati. Il processo è tanto illuminante quanto il prodotto.

### Ulteriori Risorse <a href="#furtherresourcsupervisedclassifiers" id="furtherresourcsupervisedclassifiers"></a>

* [Matthew L. Jockers](https://orcid.org/0000-0001-5599-3706) ha una serie di post sul suo progetto di sentiment analysis che inizia [qui](https://www.matthewjockers.net/2015/02/02/syuzhet/). In questi post trovi la connessione alla clip di Vonnegut.
* [Lessici del sentimento specifici del dominio per le scienze sociali computazionali](https://nlp.stanford.edu/projects/socialsent/).
