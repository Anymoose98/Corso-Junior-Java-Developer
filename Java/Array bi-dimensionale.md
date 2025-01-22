# **Cos'è?** 
Un **array bidimensionale** (o matrice) in Java è una struttura che consente di organizzare i dati in righe e colonne, come una tabella. Ecco come funzionano e alcuni esempi utili per lavorarci.

---

# **Componenti principali:**
1. **Nome dell'Array**
    - Identifica l'array bidimensionale e permette di accedervi.  
    
2. **Dimensione dell'Array**
    - Specifica il numero di righe e colonne (lunghezza e larghezza) che l'array può contenere.  

3. **Tipo di Dati**
    - Determina i tipi di dati che l'array può memorizzare.  
        
4. **Righe e Colonne**
    - Ogni elemento dell'array è identificato da una coppia di indici: il primo rappresenta la riga e il secondo la colonna.  


---

## **Sintassi:**

````java
// Dichiarazione e inizializzazione 
int[][] nome = 
{ 
	{1, 2, 3}, 
	{4, 5, 6}, 
	{7, 8, 9} 
};
````

````java
// Dichiarazione 
int[][] nome = new int[3][3]; 

// Inizializzazione
nome[0][0] = 1; // Prima riga, prima colonna
nome[0][1] = 2; // Prima riga, seconda colonna
nome[2][2] = 9; // Terza riga, terza colonna
````

````java
int[][] nome = 
{ 
	{1, 2, 3}, 
	{4, 5, 6}, 
	{7, 8, 9} 
}; 

// Accesso a tutta la prima riga 
System.out.println(Arrays.toString(nome[0])); // Output: [1, 2, 3]

// Accesso a la prima riga elemento 2
System.out.println(nome[0][1]); // Output: 2 (prima riga, seconda colonna)
````


> [!warning]
> Gli array bidimensionali possono avere anche più dimensioni 
> ````Java
> int[][][] nome = 
> { 
> 	{ 
> 		{1, 2, 3}, 
> 		{4, 5, 6},
> 		{7, 8, 9} 
> 	}, 
> 	{ 
> 		{10, 11, 12}, 
> 		{13, 14, 15}, 
> 		{16, 17, 18} 
> 	}, 
> 	{ 
> 		{19, 20, 21}, 
> 		{22, 23, 24}, 
> 		{25, 26, 27} 
> 	} 
> };
> System.out.println(matrice[0][1][2]); // Stampa: 6

