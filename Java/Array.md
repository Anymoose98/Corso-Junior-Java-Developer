# **Cos'è?** 
Gli `array` servono a memorizzare e gestire una raccolta di valori dello stesso tipo in una singola struttura, accessibili tramite un indice numerico che parte da 0.
Sono utili quando devi lavorare con più dati correlati (es. una lista di numeri, nomi o oggetti) e permettono operazioni come aggiungere, leggere, modificare o iterare facilmente sui valori.

---

# **Componenti principali:**
1. **Nome dell'Array**
	- Identifica l'array e permette di accedervi.
2. **Dimensione dell'Array**
	- Specifica quanti elementi l'array può contenere.
3. **Tipo di Dati**
	-  Determina i [[Tipi di dati (java)]] che l'array può memorizzare. 

> [!warning]
> Ricorda: gli array partono da indice 0

| Indice | Valore |
| :----: | ------ |
|   0    | nome1  |
|   1    | nome2  |
|   2    | nome3  |

---

# **Sintassi:**

##### Stringhe
````Java
// Dichiarazione e inizializzazione 
String[] nomi = {"nome0", "nome1", "nome2"}; 
````

````java
// Dichiarazione
String[] nomi = new String[5];
// inizializzazione
nomi[2]= "nome2";
````

````Java
// Accesso agli elementi 
System.out.println(nomi[0]); // Output: nome0
````
##### Numeri
````java
// Dichiarazione e inizializzazione 
int[] numeri = {10, 20, 30, 40, 50}; 
````

````java
// Dichiarazione 
int[] numeri = new int[5]; 
// Inizializzazione 
numeri[2] = 30;
````

````Java
// Accesso agli elementi 
System.out.println(numeri[2]); // Output: 30
````

---

# **Mostrare un array completo**

````java
for (int i = 0; i < nomi.length; i++) {
System.out.println(nomi[i]);
}
````

# Metodi utili
[[Filter]]
[[Map]]
[[Reduced]]
[[Sorted]]
