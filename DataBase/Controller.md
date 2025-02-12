# **Cos'è?**
Un **controller** è una classe che gestisce le richieste HTTP e funge da intermediario tra il client e il servizio (service) o il livello di accesso ai dati ([[Creare la repository]]).

---
# **Componenti principali:**
1. `@RestController`: Indica che questa classe è un controller REST e restituisce dati.
2. `@GetMapping`, `@PostMapping`, `@PutMapping`, `@DeleteMapping` che Specificano il tipo di [[Metodi HTTP]] gestita.
3. `@RequestMapping("/api")` (Non è obbligatorio) Definisce il percorso base per le richieste
---
# **Sintassi:**

### Base:
````JAVA
// Indica che questa classe è un controller REST 
@RestController 
// Definisce il percorso base per le richieste public class 
HelloController { 
	// Gestisce le richieste GET su /hello
	@GetMapping("/hello")  
	public String sayHello() { 
	return "Ciao! Benvenuto in Spring Boot! 🚀"; 
	} 
}
````

### Con il request Mapping:
````JAVA
// Indica che questa classe è un controller REST 
@RestController 

// Definisce il percorso base per le richieste
@RequestMapping("/api")

// Definisce il percorso base per le richieste public class 
HelloController { 
	// Gestisce le richieste GET su /api/hello
	@GetMapping("/hello")  
	public String sayHello() { 
	return "Ciao! Benvenuto in Spring Boot! 🚀"; 
	} 
}
````
### Con richiesta URL
````JAVA
@RestController
@RequestMapping("/api")
public class UserController {
	// Gestisce GET /api/user/{id}
	@GetMapping("/user/{id}") 
	public String getUserById(@PathVariable int id) {
		return "Utente con ID: " + id;
	}
	// Gestisce GET /api/user?name=Daniel
	@GetMapping("/user") 
	public String getUserByName(@RequestParam String name) {
		//return = Ciao Daniel, benvenuto
		return "Ciao " + name + ", benvenuto!";
	}
}	
````
