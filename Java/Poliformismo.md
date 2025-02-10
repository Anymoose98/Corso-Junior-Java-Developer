# **Cos'è?**
Il **polimorfismo** in Java è un concetto fondamentale della programmazione orientata agli oggetti. Consente agli oggetti di essere trattati in modi diversi a seconda del loro tipo reale, pur utilizzando un'interfaccia o una classe base comune.

---
# **Esempio pratico:**
````Java
// Classe base
class Animal {
    void sound() {
        System.out.println("Verso generico di un animale");
    }
}

// Classe derivata: Dog
class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Bau");
    }
}

// Classe derivata: Cat
class Cat extends Animal {
    @Override
    void sound() {
        System.out.println("Miao");
    }
}

// Classe principale
public class Main {
    public static void main(String[] args) {
        // Polimorfismo dinamico
        Animal myAnimal;

        // Istanza di Dog
        myAnimal = new Dog();
        myAnimal.sound(); // Output: Bau

        // Istanza di Cat
        myAnimal = new Cat();
        myAnimal.sound(); // Output: Miao

        // Istanza generica di Animal
        myAnimal = new Animal();
        myAnimal.sound(); // Output: Verso generico di un animale
    }
}
````
