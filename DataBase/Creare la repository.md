## Cos'è?
È un'interfaccia che fornisce metodi per effettuare operazioni [[CRUD]] (Create, Read, Update, Delete) sulle entità. Spring Data JPA (o altre librerie di persistenza) si occupa di implementare queste operazioni automaticamente.

---
# Metodi disponibili

| Metodo JPA     | Funzione                   |
| -------------- | -------------------------- |
| save(entity)   | Salva o aggiorna un'entità |
| findById(id)   | Trova un'entità per ID     |
| findAll()      | Trova tutte le entità      |
| delete(entity) | Elimina un'entità          |
| deleteById(id) | Elimina per ID             |

---
# Sintassi
Esempio
````Java
package com.example.demo.repository; 
import com.example.demo.model.User; 
import org.springframework.data.jpa.repository.JpaRepository; 
import org.springframework.stereotype.Repository;

@Repository 
public interface UserRepository extends JpaRepository<User, Long> { 
	// Esempio di Query automatica
	User findByEmail(String email);
}
````

## Entità dell'esempio
````Java
package com.example.demo.model;
import jakarta.persistence.*;

@Entity 
@Table(name = "users") 
public class User {
	@Id 
	@GeneratedValue(strategy = GenerationType.IDENTITY) 
	private Long id;

	@Column(nullable = false, length = 100) 
	private String name;

	@Column(nullable = false, unique = true, length = 150) 
	private String email;

	// Costruttori 
	public User() {}

	public User(String name, String email) { 
	this.name = name; 
	this.email = email; 
	}

	// Getters e Setters 
	public Long getId() { 
		return id; 
	}
	public void setId(Long id) { 
		this.id = id; 
	}
	//ecc.
````