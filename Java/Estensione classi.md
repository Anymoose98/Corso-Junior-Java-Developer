# **Cos'è?**
L’**estensione di una classe** (o **ereditarietà**) è un concetto chiave della programmazione orientata agli oggetti (OOP) che consente a una classe (detta **sottoclasse** o **classe derivata**) di **ereditare** attributi e metodi da un’altra classe (detta **superclasse** o **classe base**).  
Questo meccanismo consente di riutilizzare il codice, estendere funzionalità esistenti e favorire la modularità del progetto.

---
# **Componenti principali:**
- **Superclasse**
    - La classe da cui una sottoclasse eredita. Contiene attributi e metodi comuni a tutte le sottoclassi.
    - Dichiarata normalmente con la parola chiave `class`.
- **Sottoclasse**
    - La classe che estende una superclasse, ereditandone proprietà e metodi. Può aggiungere o sovrascrivere comportamenti specifici.
    - Si definisce con la parola chiave `extends`.
- **Sovrascrittura dei metodi (Override)**
    - Permette di ridefinire un metodo della superclasse nella sottoclasse per personalizzarne il comportamento.
- **Parola chiave `super`**
    - Utilizzata per riferirsi alla superclasse, come ad esempio per chiamare il costruttore o i metodi della superclasse.
- **Ereditarietà singola**
    - In Java, una classe può estendere **solo una superclasse** (Java non supporta l’ereditarietà multipla con classi, ma supporta le interfacce per ottenere un effetto simile).

---
# **Sintassi:**
## Creiamo la super classe
````Java
// Superclasse 
public class Veicolo { 
	// Attributi 
	String marca; 
	String modello;
	 
	// Costruttore 
	public Veicolo(String marca, String modello) { 
		this.marca = marca; 
		this.modello = modello; 
	} 
	
	// Metodo 
	public void dettagliVeicolo() { 
	System.out.println("Il veicolo è una " + marca + " modello " + modello); 
	} 
}
````
## Creiamo un'estensione della classe
````Java
// Sottoclasse 
public class Camion extends Veicolo { 
	// Attributo specifico 
	int capacitaCarico; 
	
	// Costruttore 
	public Camion(String marca, String modello, int capacitaCarico) { 
		super(marca, modello); // Chiama il costruttore della superclasse 
		this.capacitaCarico = capacitaCarico; 
	} 
	
	// Metodo specifico 
	public void dettagliCamion() { 
	System.out.println("Il camion è una " + marca + " modello " + modello + " con una       capacità di carico di " + capacitaCarico + " tonnellate."); 
	} 
}
````

## Creazione e utilizzo di un oggetto della sottoclasse
````Java
public class Main { 
	public static void main(String[] args) { 
	
	// Creazione di un oggetto 
	Camion camion1 = new Camion("Volvo", "FH16", 20); 
	
	// Metodo ereditato dalla superclasse 
	camion1.dettagliVeicolo(); // Output: Il veicolo è una Volvo modello FH16 
	
	// Metodo specifico della sottoclasse 
	camion1.dettagliCamion(); 
	// Output: Il camion è una Volvo modello FH16 con una capacità di carico di 20          tonnellate. 
	} 
}
````
