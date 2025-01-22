# **Cos'è?**
In Java, il metodo `.map()` è una funzione tipica delle librerie di programmazione funzionale, come quelle fornite da Java Streams. A differenza del ciclo `for`, che è una struttura imperativa, `.map()` consente di trasformare elementi di una collezione in modo più dichiarativo e funzionale.

---

# **Componenti principali:**
1. **Collezione o Flusso**: La sorgente dei dati da trasformare, come una lista, un array o un flusso.
2. **Funzione di trasformazione**: Una funzione lambda o una referenza a metodo che specifica come trasformare ogni elemento.
3. **Risultato**: Un nuovo flusso (o collezione se lo raccogli) con gli elementi trasformati.

---

# **Sintassi:**
````Java
// Dichiarazione e inizializzazione
List<Integer> numeri = Arrays.asList(1, 2, 3, 4, 5);
````

````Java
// Eseguo il .map
numeri.stream()
      .map(numero -> numero * 2) // Trasforma ogni numero moltiplicandolo per 2
      .collect(Collectors.toList()); // Raccoglie in una nuova lista
````

````Java
// Stampo il risultato 
System.out.println(numeriDoppi); // Output: [2, 4, 6, 8, 10]
````
