# CheckTelefono

Ricevuto come parametro un vettore di string, ritornare al chiamante la prima stringa che assomiglia molto ad un numero di telefono cellulare italiano ovvero:
- che inizia con +39 (esattamente lungo  13)
- oppure con 0039 (esattamente lungo 14)
- oppure con un 3 (esattamente lungo 10)

Se il numero non viene trovato, ritornare stringa vuota ""

## Codice


    for (int i = 0; i < input.Length; i++ ) {

        string n = input[i];

        if (
            (n.Length == 13 && n.StartsWith("+39"))||
            (n.Length == 10 && n.StartsWith("3"))||
            (n.Length == 14 && n.StartsWith("0039"))||
            (n.Length == 13 && n.StartsWith("001"))
            )

        {

            return n;

        }

    }

    return "";
    }

## Spiegazione codice

 La funzione accetta un parametro chiamato "input", poi il codice esegue un ciclo for per iterare attraverso gli elementi nella collezione input esso viene eseguito finché "i" è minore della lunghezza di input.
All'interno del ciclo, viene estratta una stringa n dall'elemento corrente di input usando l'indice "i". Quindi, il codice verifica se "n" soddisfa una delle seguenti condizioni:
-La lunghezza di n è 13 e inizia con "+39".
-La lunghezza di n è 10 e inizia con "3".
-La lunghezza di n è 14 e inizia con "0039".
-La lunghezza di n è 13 e inizia con "001".
Se una qualsiasi di queste condizioni è vera per la stringa n, la funzione restituirà immediatamente n, interrompendo il ciclo for. In caso contrario, se nessuna di queste condizioni è vera per tutte le stringhe in input, la funzione restituirà una stringa vuota ("").
