
# Schema Riassuntivo

| Tipologia | Descrizione                                  | Esempio                             |
| --------- | -------------------------------------------- | ----------------------------------- |
| 1 a 1     | Un record in A corrisponde a uno in B        | Utenti ↔ Profili                    |
| 1 a N     | Un record in A corrisponde a molti in B      | Categorie ↔ Prodotti                |
| N a N     | Molti record in A corrispondono a molti in B | Studenti ↔ Corsi tramite Iscrizioni |

# **Relazione 1 a 1 (One-to-One)**

In una relazione 1 a 1, a un record di una tabella corrisponde esattamente un record di un'altra tabella. Questo tipo di relazione viene usato per suddividere i dati in più tabelle per ragioni di ottimizzazione o sicurezza.

## **Esempio**  
Tabella **Utenti** e Tabella **Profili**:
- Ogni utente ha un solo profilo, e ogni profilo appartiene a un solo utente.

**Struttura**
- **Utenti** (`id`, `nome`, `email`)
- **Profili** (`id`, `utente_id`, `foto`, `biografia`)

**Relazione**:  
`Utenti.id` → `Profili.utente_id`

---

# Relazione 1 a N (One-to-Many)

In una relazione 1 a N, un record di una tabella può essere associato a più record di un'altra tabella, ma ogni record della seconda tabella è associato a un solo record della prima tabella. È il tipo di relazione più comune.

## **Esempio**  
Tabella **Categorie** e Tabella **Prodotti**:
- Una categoria può avere molti prodotti, ma ogni prodotto appartiene a una sola categoria.

**Struttura**
- **Categorie** (`id`, `nome`)
- **Prodotti** (`id`, `categoria_id`, `nome`, `prezzo`)

**Relazione**:  
`Categorie.id` → `Prodotti.categoria_id`

---
# Relazione N a N (Many-to-Many)

In una relazione N a N, più record di una tabella possono essere associati a più record di un'altra tabella. Questo tipo di relazione viene gestito tramite una tabella di associazione (pivot table) che collega i record delle due tabelle principali.

## **Esempio**  
Tabella **Studenti** e Tabella **Corsi**:
- Uno studente può iscriversi a più corsi, e ogni corso può avere più studenti.

**Struttura**
- **Studenti** (`id`, `nome`)
- **Corsi** (`id`, `nome`)
- **Iscrizioni** (`studente_id`, `corso_id`)

**Relazione**:  
`Studenti.id` → `Iscrizioni.studente_id`  
`Corsi.id` → `Iscrizioni.corso_id`

---