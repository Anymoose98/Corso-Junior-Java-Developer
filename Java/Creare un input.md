> [!warning]
> Ricordati di importare lo scanner:
> ```Java
import java.util.Scanner;

## Crea un nuovo oggetto Scanner per leggere l'input dell'utente da tastiera.
```Java 
Scanner sc = new Scanner(System.in); 
```

## Stampa la richiesta all'utente
```Java 
System.out.println("Testo che vuoi"); 
```

## Legge una riga di testo inserita dall'utente
Sostituire nextLine con il codice più appropriato 
```Java
nome1 = sc.nextLine()
```

| Metodo           | Tipo restituito | Dettagli                                                                                            |
| ---------------- | --------------- | --------------------------------------------------------------------------------------------------- |
| sc.nextInt()     | int             | Legge un numero intero.                                                                             |
| sc.nextDouble()  | double          | Legge un numero decimale                                                                            |
| sc.nextFloat()   | float           | Legge un numero decimale in formato float (meno preciso di `double`).                               |
| sc.nextLine      | String          | Legge l'intera riga di testo (fino al carattere \n).                                                |
| sc.next()        | String          | Legge la prossima "parola" (delimitata da spazi o caratteri speciali, **non legge l'intera riga**). |
| sc.nextLong()    | long            | Legge un numero intero più grande rispetto a int.                                                   |
| sc.nextBoolean() | boolean         | Legge un valore booleano (true o false).\|                                                          |

> [!warning]
> Dopo i numeri e i booleani usare:
> ````Java
sc.nextLine();

## Chiudi lo scanner
```Java 
sc.close()
```