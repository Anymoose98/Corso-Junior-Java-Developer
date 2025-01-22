Un **`enum`** (abbreviazione di _enumeration_) in Java è un tipo di dato speciale che rappresenta un insieme di costanti predefinite. Viene utilizzato quando una variabile può assumere solo un numero limitato di valori distinti e definiti in anticipo, ad esempio giorni della settimana, stati di un processo o categorie di oggetti.

---
## **Sintassi nel crearlo**

Puoi anche scriverlo in un altro file e richiamarlo 

````Java
public enum Nome {
    nome1, nome2;
}
````

## **Sintassi per richiamarlo**

````Java
System.out.println("0 nome1");
System.out.println("1 nome2");

byte nomeNum = sc.nextByte();
Nome risposta = Nome.values()[nomeNum];
sc.nextLine();
````

> [!warning]
> Enum non sono stringhe normali di conseguenza per confortarle usare
> ````Java
> if (risposta == Nome.si) {
> //codice da eseguire
> }



