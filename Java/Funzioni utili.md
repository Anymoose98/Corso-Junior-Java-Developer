# **Esporre il risultato**
##### serve per inviare un messaggio alla console. Aggiunge automaticamente un ritorno a capo dopo aver stampato il testo.

Porta a capo dopo

````Java
System.out.println("testo da esporre" + variabile); 
````

Continua sulla stessa linea

````Java
System.out.print("testo da esporre" + variabile); 
````

# **Creare un numero casuale**
##### `Math.random()` è un metodo statico della classe Math che genera un valore casuale di double.
Sotto crea un double tra **0.0** (incluso) e **1.0** (escluso).

```Java
Math.random();
```

##### Moltiplicare il risultato di `Math.random()` per un valore consente di aumentare il range dei numeri. 
Sotto crea un numero tra 0.0 e 100.999.

````Java
Math.random() * 101 
````

##### Il casting `(int)` converte il numero decimale generato in un intero, eliminando la parte decimale (tronca il numero, non arrotonda). 
Sotto crea un numero tra 0 e 100

````Java
(int) (Math.random() * 101);
````

##### Scegliere un intervallo di numeri con `Math.random()` interi con un semplice calcolo matematico 
Sotto crea un numero casuale tra 10 e 50

````Java
(int) (Math.random() * (50 - 10 + 1)) + 10;
````


# **Contare un array**

In Java, la proprietà `.length` restituisce il numero di elementi di un array.

````Java
nomi.lenth
````

````Java
//Esempio
String[] nomi = {"Nome0", "Nome1", "Nome2"}; 
System.out.println(nomi.length); // Output: 3
````

# **Arrotondare dopo la virgola**

In Java, il formato `"%.2f"` è utilizzato per formattare i numeri in virgola mobile (`float` o `double`) in modo che vengano mostrati con **due cifre decimali**. È particolarmente utile per rappresentare valori come prezzi o risultati di calcoli con una precisione specifica.
Il numero `2` può essere sostituito in base a quanti numeri dopo la virgola si desiderano.

````java
double numero = 123.456789;
````

```` java
String.format("%.2f", numero))
````

# **Ricerca array ordinato**

Il metodo `Arrays.binarySearch` in Java è utilizzato per cercare un elemento all'interno di un [[array]] ordinato. È fornito dalla classe `java.util.Arrays` e implementa l'algoritmo di ricerca binaria, che è molto efficiente.
Il valore restituito sarà l'indice dell'elemento, se trovato o un numero negativo, se l'elemento non è presente.

```` java
int Arrays.binarySearch(array, chiave);
````

Esempio:
```` java
// Array ordinato 
int[] numeri = {10, 20, 30, 40, 50}; 

// Ricerca di un elemento esistente 
int indice1 = Arrays.binarySearch(numeri, 30); 
System.out.println("Elemento trovato all'indice: " + indice1);  // Output: 2 

// Ricerca di un elemento inesistente 
int indice2 = Arrays.binarySearch(numeri, 25); 
System.out.println("Elemento non trovato. Valore restituito: " + indice2); // Output: -3
````

> [!warning]
> ricorda per poterlo utilizzare devi usare:
> ```` java
> import java.util.Arrays;