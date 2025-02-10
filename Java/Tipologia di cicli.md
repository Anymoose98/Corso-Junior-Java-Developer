
> [!warning]
> Se usiamo un Return bloccherà il ciclo
# **Ciclo `do-while`**

Il **ciclo `do-while`** è una struttura di controllo che:  
- Esegue un blocco di codice **almeno una volta**, indipendentemente dalla condizione.  
- Dopo la prima esecuzione, verifica una **condizione** booleana per decidere se ripetere o terminare il ciclo.

---

### **Componenti principali:**

1. **`do`**  
   - Indica l'inizio del ciclo.  
   - Contiene il **corpo del ciclo** (il codice da eseguire).  

2. **`condizione`**  
   - È un'espressione booleana costruita con [[Operatori logici]] e/o [[Operatori di confronto]].  
   - **Se è `true`:** il ciclo si ripete.  
   - **Se è `false`:** il ciclo termina.  

---

### **Sintassi:**

```java
do {
    // Corpo del ciclo: codice da eseguire
} while (condizione);
```


# **Ciclo `Switch`** 

Lo `switch` in programmazione è una struttura di controllo che consente di gestire decisioni multiple in base al valore di una variabile o di un'espressione. È classificato come una **struttura di selezione multipla** o **decisionale**, utilizzata per eseguire blocchi di codice diversi a seconda del valore valutato.

---

### **Componenti principali:**

1. **`switch`**
    
    - Avvia la struttura di controllo.
    - Contiene la variabile o l'espressione da confrontare con i diversi **casi**.
2. **`case`**
    
    - Definisce un valore specifico con cui confrontare la variabile o l'espressione.
    - Se c'è una corrispondenza, il codice associato al `case` viene eseguito.
    - Termina con il comando **`break`** per evitare l'esecuzione dei casi successivi (fall-through).
3. **`default`** _(opzionale)_
    
    - Blocca di codice eseguito se nessun caso corrisponde al valore della variabile o dell'espressione.

---

### **Sintassi:**

````Java
switch (espressione) {
    case valore1:
        // Codice da eseguire se espressione === valore1
        break;
    case valore2:
        // Codice da eseguire se espressione === valore2
        break;
    default:
        // Codice da eseguire se nessuna corrispondenza
}
````

# **Ciclo `for`** 

Il **ciclo `for`** è una struttura di controllo che:

- Ripete un blocco di codice per un numero specifico di iterazioni.
- Utilizza una **variabile di controllo** per gestire il numero di esecuzioni, incrementandola o modificandola ad ogni passaggio.

---

### **Componenti principali:**

1. **Inizializzazione**
    - Definisce e assegna un valore iniziale alla **variabile di controllo**.
    - Questa operazione viene eseguita una sola volta all’inizio del ciclo.
2. **Condizione**
    - È un'espressione booleana costruita con [[Operatori logici]] e/o [[Operatori di confronto]].
    - **Se è `true`:** il ciclo continua.
    - **Se è `false`:** il ciclo termina.
3. **Incremento/Decremento**
    - Aggiorna il valore della variabile di controllo a ogni iterazione (ad esempio, incrementandolo o decrementandolo).
4. **Corpo del ciclo**
    - Contiene il codice da eseguire a ogni iterazione.

---

### **Sintassi:**

````java
for (int i = 0; i < 5; i++) {
    // Corpo del ciclo: codice da eseguire
}
````

