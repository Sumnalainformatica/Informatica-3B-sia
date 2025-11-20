# Informatica-3B-sia
<!--
author:   Sumna Begom

email:    sumna.begom@savoiabenincasa.it

version:  0.0.1

language: it

narrator: IT Italian Female

comment:  Quaderno elettronico di Informatica. Classe 3za. Capitolo 4. Il linguaggio C++.

import: https://raw.githubusercontent.com/LiaScript/CodeRunner/master/README.md

import: https://raw.githubusercontent.com/liascript-templates/plantUML/master/README.md

-->

# Il linguaggio C++

[Visualizza su LiaScript](https://liascript.github.io/course/?https://raw.githubusercontent.com/gionatamassibenincasa/as-25-26/refs/heads/main/3bsia/quaderno/README.md#1)

Appunti del capitolo 4 del libro di testo pp. 86--121.

Per ogni programma presentato nel testo (pp. 86, 93, 98, 99, 103, 105, 106, 107, 109, 110, 112, 115, 118, 119, 121):

1. **Predict** Esamina il programma e cerca di capire cosa farà;
2. Copia il programma in modo da poterlo eseguire sul computer; eseguilo per verificare la previsione; 
3. **Investigate** Copia il programma su PythonTutor/linguaggio C++ ed esegui passo passo il programma per comprendere come evolve il processo generato dal programma. Controlla l'evoluzione della memoria ad ogni operazione di assegnamento; Copia il link dell'esecuzione del programma (Generate embed code).
4. **Modify** Modifica il codice cambiando prima qualcosa di semplice, quindi apportate sempre più modifiche per appropriarti poco alla volta del codice sorgente. Ad esempio, se il programma usa dati scritti nel codice sorgente, modifica il programma per chiedere i dati tramite un'istruzione di input; se un programma usa valori di tipo intero, prova a sostituirli con numeri in virgola mobile...
5. **Make** Scrivi un nuovo programma, in cui puoi prendere in prestito frammenti di codice dal programma originale, che realizza una funzione diversa, oppure la stessa funzione applicata in un contesto, o problema, diverso.

## Le basi del linguaggio

Es. pag 86

### Programma a pag. 86 - Somma.cpp

``` c +Somma.cpp
// Somma.cpp
#include <iostream>
using namespace std;

int main() {
    int a, b, s;
    cin >> a;
    cin >> b;
    s = a + b;
    cout << s;

    return 0;
}
```
@LIA.cpp

#### 1. Predict (p. 86)

Il programma dichiara tre variabili intere, `a`, `b` e `s`.
Legge due numeri interi dati in ingresso memorizzandoli nelle variabili `a` e `b`, calcola la somma di queste due variabili memorizzandola in `s` e ne stampa il valore.

#### 2. Run (p. 86)

Il programma conferma la previsione

#### 3. Investigate (p. 86)

``` cpp +Somma.cpp
// Somma.cpp
#include <iostream>
using namespace std;

int main() {
    int a, b, s;
    cin >> a;
    cin >> b;
    s = a + b;
    cout << s;

    return 0;
}
```
@LIA.evalWithDebug(`["Somma.cpp"]`, `g++ -g -Wall Somma.cpp -o a.out`, `./a.out`)


Per usare PythonTutor devo impostare dei valori alle variabili di input.
Uso 1 e 2.

<iframe width="800" height="500" frameborder="0" src="https://pythontutor.com/iframe-embed.html#code=%23include%20%3Ciostream%3E%0Ausing%20namespace%20std%3B%0A%0Aint%20main%28%29%20%7B%0A%20%20%20%20int%20a,%20b,%20s%3B%0A%20%20%20%20//cin%20%3E%3E%20a%3B%0A%20%20%20%20a%20%3D%201%3B%0A%20%20%20%20//cin%20%3E%3E%20b%3B%0A%20%20%20%20b%20%3D%202%3B%0A%20%20%20%20s%20%3D%20a%20%2B%20b%3B%0A%20%20%20%20cout%20%3C%3C%20s%3B%0A%0A%20%20%20%20return%200%3B%0A%7D&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=6&heapPrimitives=nevernest&origin=opt-frontend.js&py=cpp_g%2B%2B9.3.0&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>


#### 4. Modify  (p. 86)

Voglio aggiungere informazioni all'utente per comunicare di immettere i numeri intero, voglio essere più descrittivo e andare a capo nell'output.

``` cpp +Somma.cpp
// Somma.cpp
#include <iostream>
using namespace std;

int main() {
    int a, b, s;
    cout << "Immetti un addendo intero: ";
    cin >> a;
    cout << "Immetti un altro addendo intero: ";
    cin >> b;
    s = a + b;
    cout << "La somma di " << a << " e " << b << " e' pari a " << s << "." << endl;

    return 0;
}
```
@LIA.cpp

#### 5. Make (p. 86)

Scrivo un nuovo programma che calcola il prodotto.

``` cpp +Prodotto.cpp
// Prodotto.cpp
#include <iostream>
using namespace std;

int main() {
    int a, b, p;
    cout << "Immetti un moltiplicando intero: ";
    cin >> a;
    cout << "Immetti un altro moltiplicando intero: ";
    cin >> b;
    p = a * b;
    cout << "Il prodotto di " << a << " e " << b << " e' pari a " << p << "." << endl;
#Il linguaggio C++
##Le basi del linguaggio
###Programma a pag. 93 - Tipi.cpp
// Tipi.cpp:dimensioni     dei tipi
#include <iostream>
using namespace std;

int main () {
    cout << "Dimensioni di int: " << sizeof(int) << " byte\n";
    cout << "Dimensioni di short int: " << sizeof(short int) << " byte\n;
    cout << "Dimensioni di long int: " << sizeof(long int) << " byte\n; 
    cout << "Dimensioni di long long int: " << sizeof(long long int) << " byte\n;
    cout << "Dimensioni di float: " << sizeof(float) << " byte\n; 
    cout << "Dimensioni di double: " << sizeof(double) << " byte\n;
    cout << "Dimensioni di long double " << sizeof(long double) << " byte\n;
    cout << "Dimensioni di char " << sizeof(chair) << " byte\n;
    cout << "Dimensioni di bool " << sizeof(bool) << " byte\n;
    return 0;
}

@LIA.cpp


#### 6.Assegnazione dei valori alle variabili (pag 94)

In C++ una variabile è uno spazio di memoria identificato da un nome, all’interno del quale è possibile memorizzare un valore. Prima di poterle utilizzare, le variabili devono sempre essere dichiarate specificando il loro tipo (ad esempio int, double, char). L’assegnazione di un valore a una variabile avviene tramite l’operatore =, che copia il valore presente a destra all’interno della variabile posta a sinistra.

L’inizializzazione può avvenire direttamente nella dichiarazione oppure successivamente. Esistono diversi modi per inizializzare una variabile: quello tradizionale con l’operatore =, quello con le parentesi tonde e l’inizializzazione con parentesi graffe introdotta in C++11, che è più sicura perché evita conversioni indesiderate. È anche possibile effettuare riassegnazioni durante l’esecuzione del programma, modificando il valore precedentemente contenuto nella variabile. Inoltre, C++ permette l’assegnazione a catena, che consente di dare lo stesso valore a più variabili in una sola istruzione. Le variabili possono essere inizializzate anche mediante espressioni, e C++ esegue automaticamente conversioni tra tipi diversi quando necessario, anche se ciò può comportare perdita di precisione. È possibile assegnare il valore di una variabile a un’altra, purché i tipi siano compatibili. Infine, le costanti dichiarate con la parola chiave const possono essere inizializzate una sola volta e poi non possono più essere modificate.
``` cpp +Prodotto.cpp
#include <iostream>
using namespace std;

int main() {
    // Dichiarazione e inizializzazioni con vari metodi
    int a = 10;        // inizializzazione classica
    int b(20);         // inizializzazione con parentesi tonde
    int c{30};         // inizializzazione sicura C++11

    // Riassegnazione
    a = a + 5;         // a diventa 15

    // Assegnazione tra variabili
    b = c;             // b diventa 30

    // Assegnazione multipla
    int x, y, z;
    x = y = z = 3;     // tutte e tre valgono 3

    // Conversione implicita
    double d = a;      // 15 diventa 15.0

    // Costante
    const int MAX = 100;

    // Output finale
    cout << "a: " << a << endl;
    cout << "b: " << b << endl;
    cout << "c: " << c << endl;
    cout << "x, y, z: " << x << ", " << y << ", " << z << endl;
    cout << "d: " << d << endl;
    cout << "MAX: " << MAX << endl;

    return 0;
}
@LIA.cpp
