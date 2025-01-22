Il metodo `.sorted()` in Java è un'operazione intermedia degli stream che consente di ordinare gli elementi di uno stream. Può essere utilizzato con o senza un comparatore personalizzato, in base al tipo di dati che si desidera ordinare.

---

# **Componenti principali:**
1. **Collezione o Flusso**: La sorgente dei dati da ordinare, come una lista, un array o un flusso.  
2. **Criterio di Ordinamento**: Può essere l'ordinamento naturale degli elementi (se implementano l'interfaccia `Comparable`) oppure un comparatore personalizzato definito tramite una funzione lambda o una referenza a metodo.  
3. **Risultato**: Un nuovo flusso (o collezione se lo raccogli) con gli elementi ordinati in base al criterio specificato.

---

# **Sintassi:**
````java
stream.sorted() // Ordinamento naturale 
stream.sorted(Comparator.comparing(...)) // Ordinamento personalizzato
````

````java
// Dichiarazione e inizializzazione
List<Integer> numeri = Arrays.asList(5, 2, 8, 1, 3);
````

````java
// Ordina in ordine naturale (crescente) 
List<Integer> ordinati = numeri.stream() 
.sorted() 
.collect(Collectors.toList());
````

````java
//Espongo il risultato
System.out.println(ordinati); // Output: [1, 2, 3, 5, 8]
````

````java
//Ordine decrescente
List<Integer> ordinatiDecrescenti = numeri.stream() 
.sorted(Comparator.reverseOrder())
.collect(Collectors.toList()); 
System.out.println(ordinatiDecrescenti); // Output: [8, 5, 3, 2, 1]
````