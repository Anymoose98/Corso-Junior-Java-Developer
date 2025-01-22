# **Cos'è?** 
Un **Set** è una collezione che memorizza **solo elementi unici** e non permette duplicati.  
È utile quando devi lavorare con dati in cui la ripetizione non è ammessa (es. una lista di nomi univoci o valori distinti).  
Gli elementi in un Set non hanno un ordine specifico e non sono accessibili tramite indice.

---

# **Componenti principali:**
1. Nome del set
	  - Identifica il Set e permette di accedervi.
2. Tipo di Dati
	- Determina i tipi di dati che il Set può contenere (ad esempio interi, stringhe, oggetti).
3. Unicità degli Elementi
	- Ogni elemento è presente una sola volta.

>[!warning]
> Ricorda: Non puoi accedere direttamente agli elementi tramite indice come negli array.

---

# **Sintassi:**
>[!tip]
Per mantenere un ordine negli elementi, puoi sostituirlo al posto di `HashSet` con `LinkedHashSet`, mentre per un ordinamento naturale puoi utilizzare `TreeSet`.

##### Stringhe
````Java
// Dichiarazione e inizializzazione 
Dichiarazione e inizializzazione Set<String> nomi = new HashSet<>(); 
nomi.add("nome1"); 
nomi.add("nome2"); 
nomi.add("nome3");
````

````Java
// Accesso agli elementi (con iterazione) 
for (String nome : nomi) { 
System.out.println(nome); 
}
````
##### Numeri
````Java
// Dichiarazione e inizializzazione 
Set<Integer> numeri = new HashSet<>(); 
numeri.add(10); 
numeri.add(20); 
numeri.add(30);
````

````Java
// Accesso agli elementi (con iterazione) 
for (int numero : numeri) {
System.out.println(numero); 
}
````

# **Funzioni utili**
````Java
// Verifica se un elemento esiste 
if (numeri.contains(20)) { 
System.out.println("Il numero 20 è presente nel Set."); 
}
````

````Java
// Rimozione di un elemento 
if (nomi.remove("nome2")) { 
System.out.println("Elemento 'nome2' rimosso dal Set."); 
} else { 
System.out.println("Elemento 'nome2' non trovato nel Set."); 
}
````

````Java
// Stampare la dimensione del Set 
System.out.println("Il Set contiene " + nomi.size() + " elementi.");
````

````Java
// Cancellare tutti gli elementi del Set 
nomi.clear(); 
System.out.println("Tutti gli elementi sono stati rimossi dal Set.");
````

````Java
// Controllare se il Set è vuoto 
if (nomi.isEmpty()) { 
System.out.println("Il Set è vuoto."); 
} else { 
System.out.println("Il Set contiene ancora elementi."); 
}
````