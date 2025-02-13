# **Cos'è?**
In **HTTP**, un **DELETE** è un metodo di richiesta utilizzato per **eliminare una risorsa** dal server.

---
# **Componenti principali:**
- `@DeleteMapping("/nomeURL")`: Espone l'endpoint con il metodo DELETE
- `@PathVariable`: Permette di specificare l'ID della risorsa da eliminare
---
# **Sintassi:**
````java
@DeleteMapping("/utente/{id}")
public String eliminaUtente(@PathVariable Long id) {
	return "Utente con ID " + id + " eliminato con successo!";
}
````
**Spiegazione:**
- Il client invia una richiesta DELETE a `/utente/1`.
- Il server riceve l'ID dell'utente da eliminare con `@PathVariable`.
- Restituisce una conferma dell'eliminazione.