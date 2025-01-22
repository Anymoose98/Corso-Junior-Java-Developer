# **Cos'è?**
In Java, il blocco **try-catch** è una struttura utilizzata per gestire le eccezioni, cioè situazioni anomale o errori che possono verificarsi durante l'esecuzione del programma. Questi errori possono interrompere il normale flusso del programma, ma utilizzando **try-catch**, è possibile gestirli in modo controllato.

---
# **Componenti principali:**
- **try**:
    - Contiene il blocco di codice che vuoi monitorare per eventuali eccezioni.
    - Se un'eccezione viene sollevata (thrown) all'interno di questo blocco, l'esecuzione del codice si interrompe e passa direttamente al blocco `catch` corrispondente.
- **catch**:
    - Contiene il codice per gestire l'eccezione.
    - Può avere un parametro che rappresenta l'eccezione catturata, ad esempio `ExceptionType e`, dove `e` è un oggetto che fornisce dettagli sull'errore.
- **finaly**:
	- Contiene il codice che viene eseguito a prescindere.
	- Non è obbligatorio
---
# **Sintassi:**
````Java
try { 
	int result = 10 / 2; 
} catch (ArithmeticException e) { 
	System.out.println("Errore: Divisione per zero!"); 
} finally { 
	System.out.println("Questo viene sempre eseguito."); 
}
````

````Java
// Esempio
try { int[] numbers = {1, 2, 3}; 
	 System.out.println(numbers[5]);
} catch (ArithmeticException e) { 
	System.out.println("Errore matematico."); 
} catch (ArrayIndexOutOfBoundsException e) { 
	System.out.println("Errore: Indice fuori dai limiti."); 
} catch (Exception e) { 
System.out.println("Errore generico."); 
} finally { 
	System.out.println("Questo viene sempre eseguito."); 
}
````