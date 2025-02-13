# **Cos'è?**
In **HTTP**, un **PUT** è un metodo di richiesta utilizzato per **aggiornare una risorsa esistente** sul server. Se la risorsa non esiste, in alcuni casi può essere creata.

---
# **Componenti principali:**
- `@PutMapping("/nomeURL")`: Espone l'endpoint con il metodo PUT
- `@PathVariable`: Permette di specificare l'ID della risorsa da aggiornare
- `@RequestBody`: Permette di ricevere l'oggetto JSON aggiornato
---
# **Sintassi:**
````java
@PutMapping("/utente/{id}") 
public String aggiornaUtente(@PathVariable Long id, @RequestBody Utente utente) { 
	return "Utente con ID " + id + " aggiornato a nome: " + utente.getNome(); 
}
````
**Spiegazione:** 
- Il client invia un oggetto JSON aggiornato (es. `{ "nome": "Luca" }`).
- Il server riceve l'ID dalla **URL** (`/utente/1`) e l'oggetto aggiornato con `@RequestBody`.
- Restituisce una conferma dell'aggiornamento.