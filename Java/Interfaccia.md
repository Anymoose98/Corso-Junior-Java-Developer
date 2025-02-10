# **Cos'è?**
un'interfaccia è un tipo speciale di classe astratta che definisce un contratto che altre classi devono rispettare. Contiene solo **metodi senza implementazione**. **Separano il "cosa fare" dal "come farlo"**, migliorando la manutenibilità del codice.

---
# **Componenti principali:**
1. **Definisce un comportamento comune**: Una classe che implementa un'interfaccia è obbligata a fornire un'implementazione di tutti i suoi metodi.
2. **Supporta il concetto di polimorfismo**: Un'interfaccia permette a classi diverse di essere trattate in modo uniforme.
3. **Non può avere costruttori**: Non può essere istanziata direttamente.
---
# **Sintassi:**

## Dichiarazione
````Java
// Dichiarazione di un'interfaccia 
public interface Animale { 
	void faiVerso(); // Metodo astratto 
}
````

## Classe che implementa
````Java
// Classe che implementa l'interfaccia 
class Cane implements Animale { 
	public void faiVerso() { 
		System.out.println("Bau Bau!"); 
		} 
}

class Gatto implements Animale { 
	public void faiVerso() { 
		System.out.println("Miao Miao!"); 
		} 
}
````

## Uso
````Java
// Uso dell'interfaccia 
public class Main { 
	public static void main(String[] args) { 
	
	Animale mioCane = new Cane(); 
	mioCane.faiVerso(); // Output: Bau Bau! 
	
	Animale mioGatto = new Gatto(); 
	mioGatto.faiVerso(); // Output: Miao Miao! 
	} 
}
````