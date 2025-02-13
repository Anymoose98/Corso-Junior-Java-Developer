# **Cos'è?**
In **HTTP**, un **POST** è un metodo di richiesta utilizzato per **inviare dati** al server e modificarne lo stato.

---
# **Componenti principali:**
- `@PostMapping("/nomeURL")`: Espone l'endpoint con il metodo POST
- `@RequestBody`: Permette di ricevere un oggetto JSON nel corpo della richiesta
---
# **Sintassi:**
````java
@PostMapping("/utente")
public String creaUtente(@RequestBody Utente utente) {
	return "Utente " + utente.getNome() + " creato con successo!";
}
````
**Spiegazione:**
- Il client invia un oggetto JSON (es. `{ "nome": "Mario" }`).
- Il server lo riceve grazie a `@RequestBody`.
- Restituisce una conferma della creazione.