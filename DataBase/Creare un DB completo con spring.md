# Comandi iniziali
Una volta aperto Visual Studio andare in alto e su "Search" (in alto centrale) eseguire i seguenti comandi
1. `>Java: create java project`
2. `Spring Boot`
3. `Maven Project`
4. `3.4.1`
5. `Java`
6. `com.github.anymoose98.nomeProggetto` Per convenzione si tende a mettere il dominio di github al contrario (o un dominio a piacere)con il proprio nome e poi il nome del progetto .
7. `nomedelprogetto` Attenzione alle maiuscole e caratteri speciali
8. `Jar`
9. `21` Potete scegliere anche un'altra versione ma stava dando problemi ad alcuni.
10. Per le dependencies;
- `MySQL Driver SQL` Aggiunge le dependencies in maniera automatica invece che manuale
- `Spring Data JPA SQL` Aggiunge le dependencies in maniera automatica invece che manuale
- Cliccare enter
11. Scegliere il posto dove salvare e cliccare open
# Aperto il progetto come collegare il server
La prima cosa da fare è andare su Java Projects come da allegato

Entrare Dentro la cartella `src/main/resources` Cliccare su `application.properties`, aggiungere e incollare il seguente codice:
```
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.datasource.url=jdbc:mysql://localhost:3306/NOME DATABASE
spring.datasource.username=IL TUO USERNAME
spring.datasource.password=LA TUA PASSWORD
spring.jpa.hibernate.ddl-auto=update
```

> [!warning]
>Aggiungere e non togliere la prima riga



Se è tutto corretto dovrebbe uscire questa schermata una volta runnato il tutto
![[Immagine2.png]]
# Creare la tabella 
1. Andare su `src/main/java` e cliccare sul "+"  **Vicino al contenuto** (NON su `src/main/java` )
2. Andare su `Package` 
3. aggiungere al percorso `.db.entity` cliccare invio e aspettare
4. Cliccare di nuovo sul "+" del `.db.entity` (il file appena creato) e cliccare Class e aggiungere il nome che si desidera
5. Inserire il seguente codice di esempio dove abbiamo inserito ID già fatto, continuare in base al compito richiesto
````Java
import jakarta.persistence.Entity;
import jakarta.persistence.GeneratedValue;
import jakarta.persistence.GenerationType;
import jakarta.persistence.Id;

@Entity
public class Robot {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private long id;
}
````
6. Per verificare se è stato fatto tutto in maniera corretta runnare il codice e andare su DBeaver se è stata creata correttamente

# Repository
1. Cliccare su "+" di `db.entity`, selezionare Package, togliere la scritta `entity` e al suo posto scrivere `repository`.
2. Cliccare la "+" di `repository` selezionare `interface`
3. Inserire il nome della `repository` con la lettera maiuscola, seguito da Repo. (Si usa Repo per convenzione)
4. Inserire con i propri dati quanto segue:
````Java
package com.github.anymoose98.prova.nomedelprogetto.db.repository;
import org.springframework.data.jpa.repository.JpaRepository;
import org.springframework.stereotype.Repository;

//Inserire il proprio percorso
import com.github.anymoose98.prova.nomedelprogetto.db.entity.Robot; 

@Repository

//Invece di RobotRepo & Robot inserire i propri dati
public interface RobotRepo extends JpaRepository<Robot,Long>{ 
}
````

# Service
1. Cliccare sul "+" di `db`, proseguire con `Package` e inserire `.service`
2. Cliccare sul "+" di `service`, proseguire cliccando `Class` e inserire il nome con la prima lettera maiuscola con vicino "Service" ES. `RobotService`
3. Inserire il codice seguente con i propri dati:
````Java
//Inserire il proprio percorso
package com.github.anymoose98.prova.nomedelprogetto.db.service;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Service;

//Inserire il proprio percorso
import com.github.anymoose98.prova.nomedelprogetto.db.repository.RobotRepo;

@Service
public class RobotService {
    @Autowired
    private RobotRepo robotRepo;
}
````
4. Possiamo creare le funzioni all'interno in questo modo:
````Java
@Service
public class RobotService {
    @Autowired
    private RobotRepo robotRepo;

    // Per inserire i dati
    public void insertRobot(Robot robot){
        robotRepo.save(robot);
    }

    // Per avere tutti i dati della tabella inseriti
    public List <Robot> findAll(){
        return robotRepo.findAll();
    }
}
````

> [!warning]
>Se non disposti bene non funzionerà la creazione del DB, di seguito in foto mostriamo la giusta configurazione.
>Controllare se la modalità di visualizzazione non sia impostata su flat
>

![[Immagine 1.png]]

# Fase di utilizzo
1. Andare sulla classe principale (quella con scritta Application)
2. Aggiungere il seguente codice con il propri dati;
````Java
//Inserire il proprio percorso
package com.github.anymoose98.prova.nomedelprogetto;
import org.springframework.boot.CommandLineRunner;
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
@SpringBootApplication


public class NomedelprogettoApplication implements CommandLineRunner{
    public static void main(String[] args) {
        SpringApplication.run(NomedelprogettoApplication.class, args);
    }
    @Override
    public void run(String... args) throws Exception {
    //Qui andremo a inserire il codice da eseguire
    }
}
````
3. Se vogliamo utilizzare le funzioni create precedentemente proseguire con lo schema sottostante
````Java
package com.github.anymoose98.prova.nomedelprogetto;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.boot.CommandLineRunner;
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication; 
import com.github.anymoose98.prova.nomedelprogetto.db.entity.Robot;
import com.github.anymoose98.prova.nomedelprogetto.db.service.RobotService; 
@SpringBootApplication

public class NomedelprogettoApplication implements CommandLineRunner{
    @Autowired
    private RobotService robotservice;
    public static void main(String[] args) {
        SpringApplication.run(NomedelprogettoApplication.class, args);
    }
    @Override
    public void run(String... args) throws Exception {
        // Inseriamo un robot
        robotservice.insertRobot(new Robot());
        
        // Stampiamo il risultato
        System.out.println(robotservice.findAll());
    }
}
````