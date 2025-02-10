# Cos'è?
Un **Service** è una classe che contiene la **logica di business** dell’applicazione.
**Serve a separare la logica di business dal controller** per mantenere il codice più pulito e organizzato.
**Interagisce con il livello di accesso ai dati (Repository)** e fornisce i dati al Controller.

---
# Sintassi:
Prendendo come esempio il model di [[Creare l’Entità (Model)]]

````Java
package com.example.demo.service;
import com.example.demo.model.User;
import com.example.demo.repository.UserRepository;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Service;

import java.util.List;
import java.util.Optional;

@Service
public class UserService {

    @Autowired
    private UserRepository userRepository;

    // Metodo per ottenere tutti gli utenti
    public List<User> getAllUsers() {
        return userRepository.findAll();
    }

    // Metodo per trovare un utente per ID
    public Optional<User> getUserById(Long id) {
        return userRepository.findById(id);
    }

    // Metodo per trovare un utente per email
    public User getUserByEmail(String email) {
        return userRepository.findByEmail(email);
    }

    // Metodo per creare un nuovo utente
    public User createUser(User user) {
        return userRepository.save(user);
    }

    // Metodo per eliminare un utente per ID
    public void deleteUser(Long id) {
        userRepository.deleteById(id);
    }
}
````

# Esempio di utilizzo
````java
package com.example.demo;

import com.example.demo.model.User;
import com.example.demo.service.UserService;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.boot.CommandLineRunner;
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

import java.util.List;
import java.util.Optional;

@SpringBootApplication
public class DemoApplication implements CommandLineRunner {

    @Autowired
    private UserService userService;

    public static void main(String[] args) {
        SpringApplication.run(DemoApplication.class, args);
    }

    @Override
    public void run(String... args) throws Exception {
        // Creazione di un nuovo utente
        User newUser = new User();
        newUser.setName("Mario Rossi");
        newUser.setEmail("mario.rossi@example.com");
        userService.createUser(newUser);
        System.out.println("✅ Utente creato: " + newUser);

        // Recuperare tutti gli utenti
        List<User> users = userService.getAllUsers();
        System.out.println("📋 Lista utenti:");
        users.forEach(System.out::println);

        // Recuperare un utente per ID
        Optional<User> foundUser = userService.getUserById(newUser.getId());
        foundUser.ifPresent(user -> System.out.println("🔍 Utente trovato: " + user));

        // Recuperare un utente per email
        User userByEmail = userService.getUserByEmail("mario.rossi@example.com");
        if (userByEmail != null) {
            System.out.println("📧 Utente trovato per email: " + userByEmail);
        }

        // Eliminare un utente
        userService.deleteUser(newUser.getId());
        System.out.println("🗑️ Utente eliminato con ID: " + newUser.getId());
    }
}
````
