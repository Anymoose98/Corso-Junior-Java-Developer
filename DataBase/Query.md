Nei database, una query è un'istruzione scritta in un linguaggio specifico, come **SQL (Structured Query Language)**, per manipolare o recuperare dati da un database.

---
# **Sintassi**
```sql
SELECT il_nome_di_quello_che_vogliamo_vedere FROM nome_db WHERE criterio_da_rispettare
````

---

# Esempi
## Recuperare tutti i dati di una tabella

````sql
SELECT * FROM utenti;
````

## Recuperare solo i dati in base a una condizione
Recuperare tutti i dati della tabella `utenti` dove l'età è maggiore di 18

```sql
SELECT * FROM utenti WHERE età > 18;
````

## Selezionare campi specifici
Seleziona solo i nomi di `customer`

```sql
SELECT first_name FROM customer;
````

## Filtrare valori sopra una soglia
Seleziona solo i superiori a 40000 di `annual_income`

```sql
SELECT * FROM customer WHERE annual_income > 40000;
````

## Filtrare valori sotto una soglia
Seleziona solo gli inferiori a 30000 di `annual_income`

```sql
SELECT * FROM customer WHERE annual_income < 30000;
````

## Filtrare valori in un intervallo
Seleziona tra 30000 e 40000 di `annual_income`

```sql
SELECT first_name FROM customer WHERE annual_income > 30000 AND annual_income < 40000;
````

