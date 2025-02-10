## Perché farlo?
Configurare il database è essenziale perché Spring Boot deve sapere:
1. **Dove si trova il database** ➝ `spring.datasource.url` indica l'indirizzo e il nome del database.
2. **Come autenticarsi** ➝ `spring.datasource.username` e `spring.datasource.password` forniscono le credenziali.
3. **Quale driver usare** ➝ `spring.datasource.driver-class-name` specifica il driver JDBC corretto.
4. **Come gestire le entità e lo schema** ➝ `spring.jpa.hibernate.ddl-auto` decide se Spring deve creare, aggiornare o lasciare invariato lo schema del database.

## Dove?
Dentro la cartella `src/main/resources` ci sarà un file chiamato `application.properties` e incollare il codice seguente:
```properties
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.datasource.url=jdbc:mysql://localhost:3306/NOME DATABASE
spring.datasource.username=IL TUO USERNAME
spring.datasource.password=LA TUA PASSWORD
spring.jpa.hibernate.ddl-auto=update
```