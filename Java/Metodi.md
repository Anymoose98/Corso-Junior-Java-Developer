# **Cos'è?**
Un **metodo** in programmazione è una funzione associata a una classe o a un oggetto. È una porzione di codice che esegue una determinata operazione o calcolo e può essere richiamata quando necessario.

In Java, i metodi sono utilizzati per definire il comportamento di un oggetto o per eseguire operazioni specifiche.

---
# **Componenti principali:**
1. **Tipo di Ritorno**
    - Specifica il tipo di dato che il metodo restituisce (es. `int`, `String`, `void` se non restituisce nulla).
2. **Nome del Metodo**
    - Identifica il metodo e consente di richiamarlo.
3.  **Parametri**
    - Sono i dati passati al metodo per personalizzare il suo comportamento.
4.  **Corpo del Metodo**
    - Contiene le istruzioni che il metodo deve eseguire.

---
# **Sintassi:**
### Base
````Java
//Sintassi base
public void stampaMessaggio() { 
System.out.println("Ciao, questo è un messaggio!"); 
}
````

````Java
// Utilizzo 
stampaMessaggio(); // Output: Ciao, questo è un messaggio!
````

### Con valori numerici all'interno
````Java
//Con valori numerici all'interno
public int somma(int a, int b) { 
return a + b; 
} 

// Utilizzo 
int risultato = somma(5, 3); 
System.out.println(risultato); // Output: 8
````

### Con valori stringhe all'interno
````Java
public void saluta(String nome) { 
System.out.println("Ciao, " + nome + "!");
} 

// Utilizzo 
saluta("Luca"); // Output: Ciao, Luca! 
saluta("Anna"); // Output: Ciao, Anna!
````
