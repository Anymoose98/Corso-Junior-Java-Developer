# **Cos'è?** 
Una **classe astratta** in Java è una classe che non può essere istanziata direttamente e serve come modello per altre classi. Può contenere sia **metodi astratti** (senza implementazione) sia **metodi concreti** (con implementazione). Viene utilizzata quando vuoi definire un comportamento comune per un gruppo di classi, ma lasciando ad esse l'implementazione di alcuni metodi specifici.

---
# **Componenti principali:**
1. **Dichiarazione della Classe Astratta**
	- Si utilizza la keyword `abstract` prima della dichiarazione della classe
	- Non può essere istanziata direttamente
2. **Metodi Astratti (Obbligatori nelle sottoclassi)**
	- Sono dichiarati senza le graffe { }
	- Devono essere implementati dalle sottoclassi (`extends`)
	- Sono definiti con la keyword `abstract`
3. Metodi concreti  (facoltativi)
	- Le sottoclassi possono usarli senza doverli ridefinire
4. Attributi (Facoltativi)
	- Può contenere variabili d'istanza o `static`
 ---
# **Sintassi:**
### Dichiarazione basica:
 ````Java
abstract class Nome{
	String nome;
}
  ````

### Dichiarazione esempio:
 ````Java
// Dichiarazione
abstract class Animale { 
	String nome; 
	// Costruttore 
	Animale(String nome) { 
	this.nome = nome; 
	}

	// Metodo astratto (da implementare nelle sottoclassi)
	abstract void verso(); 
	// Metodo concreto 
	void dormi() { 
		System.out.println(
		nome + " sta dormendo... Zzz...");
	} 
	// Metodo statico 
	static void info() { 
		System.out.println(
		"Gli animali sono esseri viventi."
		);
	} 
}
````

### Dichiarazione sottoclasse 
````java
class Cane extends Animale { 
	Cane(String nome) { 
		super(nome); 
	} 
	@Override 
	void verso() { 
	System.out.println
	(nome + " dice: Bau bau!");
	} 
}
````
### Esempio di uso
````java
public class Main { 
	public static void main(String[] args) { 
	Cane cane = new Cane("Fido"); 
	cane.verso(); 
	//Fido dice: Bau bau!
	
	cane.dormi(); 
	// Output: Fido sta dormendo... Zzz... 
	
	Animale.info(); 
	// Output: Gli animali sono esseri viventi. 
	} 
}
````