## ex 3

 1.  Vero: all'aumentare del grdo M, aumenta la complessità del modello
           (c'è maggior fit sui dati di training)
 2. Falso: lambda viene introdotto proprio per regolare la complex del modello
           (lambda prende a martellate la polinomiale)
 3.  Vero: prendo a martellate il polinomio
 4.  Vero: lambda controlla tutto
 5. Falso: mi serve per controllare la complex del modello
 6.  Vero: potrebbe non andare in overfitting
 7.  Vero: lambda fa proprio questo
 8. Falso: un lambda basso non contrasterebbe l'overfitting
 9. Falso: modificando sia M che Lambda ci sarà un compromesso che
           bilancia under e over-fitting
10.  Vero: posso usare qualsiasi funzione phi
11. Falso: dentro la phi posso mettere quello che voglio
12. Falso: perchè dovrei mettere un limite!?
13.  Vero: perchè con pochi dati e un polinomio alto, tendo ad andare in
           overfitting, quindi correggo con un lambda alto




## ex 4

1. Falso: può farlo perchè, grazie alle funzioni kernel, riesce a
          mappare l'Input-Space in un Feature-Space di dimensione
          più elevata in cui il problema è linearmente separabile
2.  Vero: la phi vegono aggiunte proprio per aumentaer la complex
          del modello, quindi la flessibilità
3.  Vero: così facendo si limita la complessità del modello aumentando
          quindi la capacità di generalizzazione sui nuovi dati
4.  Vero: come in tutti i metodi iterativi, conviene proseguire
5. Falso: non c'è relazione tra nodi e il numero di dati di training
6. Falso: dovrei guardare la Model-Assesment *senza guardare i dati di training*




## ex 5

1. Falso: vengono calcolati dal duale
2. Falso: sono punti dell'iperpiano sul margine
3. Falso: sono calcolati
4.  Vero: non ci sono problemi con i test
          (sarebbe invece stato un problema con i dati di training)
