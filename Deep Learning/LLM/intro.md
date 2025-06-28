Un Large Language Model è una funzione matematica molto sofisticata che predice qual'è la prossima parola che viene dopo ad un dato testo in input (prompt)
- gli output possibili sono tutte le parole del vocabolario (?)
- un LLM sceglie la parola con probabilità maggiore (la maggior parte delle volte) tra quelle del vocabolario
- retireando il procedimento ed aggiungendo ogni volta una parola, un LLM è in grado di produrre intere frasi (e.g. risposta ad una domanda)

...

Il training di LLM è feasible solamente se si riesce a sfruttare il parallelismo delle GPU. Tuttavia, non tutti gli LLM sono facilmente parallelizzabili nel loro training. Prima del 2017 gli LLM processavamo il testo una parola alla volta, solo con l'introduzione dell'architettura dei **Transformer** si è incomincato a poter sfruttare meglio il parallelismo e quindi a poter fare il training di LARGE language models.

I transformer non leggono il testo dall'inizio alla fine, una parola per volta. Piuttosto, lo processano tutto insieme contemporaneamente.

...

I transformer (e anche gli altri LLM) codificano una determinata parola (token) con un vettore n-dimensionale.

I transformer sfruttano una particolare operazione chiamata **Attention** che permette a tutti i vettori di una frase di interagire, cambiando cosi i valori delle loro componenti, in maniera tale da costruire un'idea di contesto e attribuire ad ogni parola il significato corretto. Tutti in parallelo!
- Le stesse parole possono corrispondere a vettori diversi in base alla semantica che la parola acquisisce nella frase ed al suo contesto
- Vettori vicini in questo spazio codificano parole semanticamente vicine

I transformer hanno poi anche una altra operazione che sfrutta una **Feedforward Neural Network**.

All'interno di un transformer operazioni di Attention e Feedforward vengono ripeteute in vari layer con l'obiettivo di capire qual'è il contesto migliore per la prossima parola da predirre dato il testo corrente.



Alla fine delle iterazioni, l'ultimo vettore dell'ultimo layer codifica la distribuzione di probabilità della prossima parola da aggiungere al testo corrente.
- questa predizione è stata influenzata dal contesto fornito da tutte le parole precedenti e dalle informazioni apprese durante il training del LLM 