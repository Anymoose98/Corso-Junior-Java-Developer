Il metodo `.reduce()` in Java è un'operazione terminale degli stream che consente di combinare tutti gli elementi di uno stream in un unico valore utilizzando una funzione di riduzione. È particolarmente utile per operazioni come somma, moltiplicazione, concatenazione di stringhe, e altre aggregazioni personalizzate.

---

# **Componenti principali:**
1. **`identity`**: Il valore iniziale (opzionale). Serve come base per l'accumulazione.
2.  **`accumulator`**: Una funzione che specifica come combinare due elementi (es., somma, prodotto).

---

# **Sintassi:**
````java
T reduce(T identity, BinaryOperator<T> accumulator);
````

````java
// Dichiarazione e inizializzazione
List<Integer> numeri = Arrays.asList(1, 2, 3, 4, 5);
````

````java
// Accumula la somma
int somma = numeri.stream() 
.reduce(0, (a, b) -> a + b); // Accumula la somma
````

````java
//Espongo il risultato
`System.out.println(somma); // Output: 15`
````
