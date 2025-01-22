# **Cos'è?** 

Una `HashMap` è una struttura dati che permette di memorizzare e gestire coppie di chiavi e valori. Ogni chiave è unica e viene associata a un valore specifico.È utile quando vuoi cercare, aggiungere o modificare rapidamente i valori utilizzando una chiave.

---

# **Componenti principali:**
1. **Chiave (Key)**  
    - Identifica in modo univoco un valore nella mappa.
2. **Valore (Value)**  
    - È il dato associato a una chiave.
3. **Coppia Chiave-Valore**  
    - Un’associazione di una chiave unica con un valore.

| Chiave  | Valore |
| :-----: | ------ |
| Chiave1 | nome1  |
| Chiave2 | nome2  |
| Chiave5 | nome3  |

>[!warning]
>**Chiave unica**: Non puoi avere due chiavi uguali. Se aggiungi un elemento con una chiave già esistente, il valore precedente sarà sovrascritto.

---
# **Sintassi:**

##### Stringhe
````Java
// Dichiarazione e inizializzazione 
LinkedHashMap<String, Integer> esempio = new LinkedHashMap<>();

esempio.put("chiave1", 10); // Chiave: chiave1, Valore: 10 
esempio.put("chiave2", 20); //Chiave: chiave2, Valore: 20
````

````Java
// Accesso a un elemento
int valore = esempio.get("chiave1"); // Output: 10
````

 ````Java
// Accesso agli elementi (con iterazione) 
for (Map.Entry<String, Integer> entry : esempio.entrySet()) { System.out.println("Chiave: " + entry.getKey() + ", Valore: " + entry.getValue()); 
} 
// Output: 
// Chiave: chiave1, Valore: 10 
// Chiave: chiave2, Valore: 20
 ````
##### Numeri
````Java
// Dichiarazione e inizializzazione 
LinkedHashMap<Integer, Integer> esempio = new LinkedHashMap<>();

esempio.put(1, 100); // Chiave: 1, Valore: 100 
esempio.put(2, 200); // Chiave: 2, Valore: 200 
esempio.put(3, 300); // Chiave: 3, Valore: 300
````

 ````Java
// Accesso a un elemento
int valore = esempio.get(2); // Output: 200
````

 ````Java
 // Accesso agli elementi (con iterazione) 
for (Map.Entry<Integer, Integer> entry : esempio.entrySet()) { System.out.println("Chiave: " + entry.getKey() + ", Valore: " + entry.getValue()); 
} 
// Output: 
// Chiave: 1, Valore: 100 
// Chiave: 2, Valore: 200 
 ````

# **Funzioni utili**
````Java
// Rimuove la chiave
map.remove("chiave1");
````

````Java
// Controlla se la chiave esiste
boolean esiste = map.containsKey("chiave2"); // Output: true
````

````Java
// Controlla se il valore esiste
boolean esisteValore = map.containsValue(20); // Output: true
````


````Java
// Controlla la dimensione della map
int dimensione = map.size(); // Output: 2
````

````Java
// Controlla se è vuota 
boolean vuota = map.isEmpty(); // Output: false
````


````Java
// Svuota la map
map.clear(); // La mappa sarà vuota
````
