Passi principali:
1. **Population creation**: crea una popolazione di N elementi, ognuno con un genotipo (valori di una qualche struttura dati (tipicamente un array per facilitare il crossover)) random
    - questo passo viene fatto una volta all'inizio

2. **Selection**: valuta ogni elmento della popolazione corrente e determina quali sono i membri che saranno i genitori della prossima generazione. Consiste in:
    1. valutare la fitness di ogni elmento
        - bisogna decidere una funzione di fitness che valuto dello stato mantenuto all'interno dell'elemento
        - il dominio della funzione di fitness sono gli elementi della popolazione, l'immagine è un numero reale
    2. crare una mating pool (lista di coppie di genitori lunga tanto quanto la dimensione della nuova generazione)
        - bisogna scegliere i genitori secondo qualche criterio che tiene della loro fitness
        - gli elementi con più fitness devono avere più probabilità di diventare genitori in quanto più adatti
        - importante mantenere varianza non escludendo a priori gli elementi con fitness bassa, altrimenti l'evoluzione si arresta. Sufficiente attribuire a quest'ultimi una probabilità bassa (ma non nulla) di diventare genitori

3. **Reproduction**: data una mating pool, come si crea la prossima generazione?   
    1. **crossover**: combinazione del genotipo di due genitori 
        - varie strategie: 50/50, random-midpoint, serie di coin-flip
        - fatto N volte per ottenere N figli per la prossima generazione
    2. **mutation**: introduce nuova varianza mutando casualmente il genotipo del figlio ottenuto tramite crossover
        - passo opzionale
        - utile se la popolazione iniziale non aveva tutti i tratti necessari per una buona soluzione
            - varianza limitata superiormente dalla popolazione iniziale, e monotona decrescente a causa della selection
         