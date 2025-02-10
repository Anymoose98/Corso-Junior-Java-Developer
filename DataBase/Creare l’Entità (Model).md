## Cos'è il model?
Il **Model** in Spring rappresenta un oggetto che definisce una tabella di un database. Viene utilizzato per gestire i dati dell'applicazione e definire la struttura.

---
## Da cosa è composto?
Un model in Spring è generalmente composta da:
1. **Annotazioni** – come `@Entity`, `@Table`, `@Id`, `@GeneratedValue` per definire la mappatura con il database.
2. **Campi (Attributi)** – che rappresentano le colonne della tabella nel database.
3. **Metodi Getter e Setter** – per accedere e modificare i dati.
4. **Costruttori** – per inizializzare l'oggetto.
5. **Metodi aggiuntivi** – come `toString()`, `equals()`, e `hashCode()` per una migliore gestione.
---
## Esempio con spiegazione
````java
import jakarta.persistence.*;

@Entity // Indica che questa classe è un'entità JPA

@Table(name = "users") // Specifica il nome della tabella nel database

public class User {
	@Id // Indica la chiave primaria
	
	@GeneratedValue(strategy = GenerationType.IDENTITY) // Auto-incremento dell'id
	
	private Long id;

	@Column(nullable = false, length = 50) // Definisce la colonna nel database 
	private String name;

	@Column(nullable = false, unique = true) // L'email deve essere univoca private String email;

	// Costruttore vuoto (obbligatorio per JPA) 
	public User() { 
	}

	// Costruttore con parametri
	public User(String name, String email) { 
	this.name = name; 
	this.email = email; 
	}

	// Getter e Setter
	public Long getId() { 
	return id; 
	}

	public void setId(Long id) { 
	this.id = id; 
	}

	public String getName() { 
	return name; 
	}

	public void setName(String name) { 
	this.name = name; 
	}

	public String getEmail() { 
	return email; 
	}

	public void setEmail(String email) { 
	this.email = email; 
	}

	// Metodo toString() per rappresentazione testuale dell'oggetto
	@Override 
	public String toString() {
	return "User{" +
	 "id=" + id +
	", name='" + name + '\'' +
	 ", email='" + email + '\'' +
	 '}';
	}
}
````