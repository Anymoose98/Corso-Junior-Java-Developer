# **Cos'è?**
Una lista è una struttura dati che consente di memorizzare e gestire una raccolta di valori dello stesso tipo in **modo dinamico**. A differenza degli array, le liste in Java possono crescere o ridursi dinamicamente durante l'esecuzione del programma, permettendo operazioni come aggiungere, leggere, modificare o rimuovere facilmente elementi. Sono utili quando si desidera una collezione che possa modificarsi nel tempo, come una lista di numeri, stringhe, oggetti, ecc.

---

# **Componenti principali:**

1.  **Nome della Lista**: 
	 - Identifica la lista e permette di accedervi.
2.  **Capacità della Lista**:
	- Indica il numero di elementi che la lista può contenere, ma a differenza degli array, le liste si adattano automaticamente al numero di elementi.
3.  **Tipo di Dati**: 
	- Definisce il [[Tipi di dati (java)]] che la lista può memorizzare (ad esempio `Integer`, `String`, `Object`).

| Indice | Valore |
| :----: | ------ |
|   0    | nome1  |
|   1    | nome2  |
|   2    | nome3  |

---

# **Sintassi:**

##### Stringhe:
````java
// Dichiarazione e inizializzazione 
ArrayList<String> nomi = Arrays.asList("Mario", "Luigi", "Giovanni");
````

````java
// Dichiarazione
ArrayList<String> nomi = new ArrayList<>(); 

// inizializzazione
nomi.add("Mario");
nomi.add("Luigi");
nomi.add("Giovanni");
````

````java
// Accesso agli elementi 
System.out.println(nomi.get(0)); // Output: Mario
````

##### Numeri

````java
// Dichiarazione e inizializzazione in un'unica riga 
ArrayList<Integer> numeri = new ArrayList<Integer>() {{ 
add(10); 
add(20); 
add(30); 
add(40); 
}};
````

````Java
// Dichiarazione 
ArrayList<Integer> numeri = new ArrayList<>(); 
// Inizializzazione
numeri.add(10); 
numeri.add(20); 
numeri.add(30); 
numeri.add(40); 
````

````Java
// Accesso agli elementi 
System.out.println(numeri.get(0)); // Output: 10
````

# **Operazioni principali sulle Liste**:

### **Aggiungere un elemento**: `add()`

````java
numeri.add(50); // Aggiunge 50 alla lista
````
### **Accedere a un elemento**: `get()`
````java
int primoNumero = numeri.get(0); // Accede al primo elemento (10)
````
### **Modificare un elemento**: `set()`
````java
numeri.set(1, 25); // Modifica il secondo elemento (20) e lo cambia in 25
````
### **Rimuovere un elemento**:`remove()`
````java
numeri.remove(2); // Rimuove l'elemento all'indice 2 (30) 
System.out.println(numeri); // Output: [10, 20, 40] 

numeri.remove(Integer.valueOf(20)); // Rimuove il valore 20 dalla lista
System.out.println(numeri); // Output: [10, 40]
````
### **Verificare la presenza di un elemento**: `contains()`
````java
boolean contiene30 = numeri.contains(30); // Verifica se 30 è presente nella lista
System.out.println(contiene30); // Output: true
````
### **Ottenere la dimensione della lista**:`size()`
````java
int dimensione = numeri.size(); // Restituisce la dimensione della lista
System.out.println(dimensione); // Output: 4 (per esempio, se la lista contiene [10, 20, 30, 40])
````