# **Cos'è?** 
Il metodo `.filter()` in Java è un'operazione intermedia degli stream utilizzata per **filtrare** gli elementi di uno stream in base a una condizione specifica (un predicato). Gli elementi che soddisfano la condizione rimangono nello stream, mentre gli altri vengono esclusi.

---

# **Componenti principali:**
1. **Input**: Una funzione lambda (o un predicato) che specifica una condizione booleana.
2.  **Output**: Un nuovo stream contenente solo gli elementi che soddisfano la condizione.

---

# **Sintassi:**
````java
//base sintassi
stream.filter(element -> condition)
````

````java
// Dichiarazione e inizializzazione 
List<Integer> numeri = Arrays.asList(1, 2, 3, 4, 5, 6);
````
````java
//controllo quali sono pari
List<Integer> numeriPari = numeri.stream() 
	.filter(numero -> numero % 2 == 0) // Condizione: numero pari 
	.collect(Collectors.toList()); 
````
````java
//espongo il risultato
System.out.println(numeriPari); // Output: [2, 4, 6]
````
