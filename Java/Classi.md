# **Cos'è?**
Una **classe** è un modello per creare oggetti. Definisce le **proprietà** (attributi) e i **comportamenti** (metodi) che gli oggetti creati da essa possono avere.  
È un concetto fondamentale della programmazione orientata agli oggetti (OOP) che consente di organizzare il codice in modo modulare e riutilizzabile.

---

# **Componenti principali:**
1. **Nome della Classe**
    - Identifica la classe e viene utilizzato per crearne le istanze (oggetti).
2. **Attributi (Proprietà)**
    - Variabili definite all'interno della classe che rappresentano lo stato o le caratteristiche dell'oggetto.
3. **Metodi (Comportamenti)**
    - Funzioni definite all'interno della classe che descrivono le operazioni che l'oggetto può eseguire.
4. **Costruttore**
    - Un metodo speciale che viene chiamato quando viene creata un'istanza della classe per inizializzarne gli attributi.

---

# **Sintassi:**
### Base
````Java
// Dichiarazione della classe 
public class Persona { 
	
	// Attributi 
	String nome; 
	int eta; 
	
	// Costruttore 
	public Persona(String nome, int eta) { 
		this.nome = nome; 
		this.eta = eta; 
	} 
	
	// Metodo 
	public void saluta() { 
		System.out.println("Ciao, mi chiamo " + nome + " e ho " + eta + " anni."); 
	} 
}
````


````Java
// Creazione di un oggetto 
Persona Persona persona1 = new Persona("Luca", 25); 
// Utilizzo del metodo 
persona1.saluta(); // Output: Ciao, mi chiamo Luca e ho 25 anni.
````

[[Estensione classi]]
[[Classe astratta]]