# **Cos'è?**
In **HTTP**, un **GET** è un metodo di richiesta utilizzato per **recuperare dati** da un server senza modificarli.

---
# **Componenti principali:**
- `@GetMapping("/nomeURL")`: Espone l'endpoint con il GET
- `@RequestParam`: Permette di passare un parametro
---
# **Sintassi:**
````java
@GetMapping("/saluto") 
public String saluta(@RequestParam(defaultValue = "Mondo") String nome) { 
return "Ciao, " + nome + "!"; //Se non passa un parametro sarà mondo di base
} 
````

