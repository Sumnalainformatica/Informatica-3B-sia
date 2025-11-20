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

[Visualizza su LiaScript](https://liascript.github.io/course/?https://raw.githubusercontent.com/Sumnalainformatica/Informatica-3B-sia/refs/heads/main/README.md)

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
```
@LIA.cpp


## Assegnazione dei valori alle variabili (pag 94)

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
```
@LIA.cpp

## il casting per conversione di tipo (p.97)

In C++ il casting è l’operazione che permette di convertire un valore da un tipo a un altro. Può essere necessario quando si combinano variabili di tipi diversi oppure quando si vuole ottenere un controllo più preciso sulla conversione. Le conversioni possono avvenire in modo implicito, quando il compilatore le esegue automaticamente, oppure in modo esplicito, quando è il programmatore a richiederle tramite un cast.

La conversione implicita avviene quando C++ può convertire in modo sicuro un tipo in un altro senza perdita di dati significativa, come da int a double. Tuttavia, quando si converte da un tipo “più grande” o più preciso ad uno “più piccolo”, come da double a int, la conversione può comportare la perdita dei decimali: per questo motivo spesso si preferisce usare il casting esplicito per indicare chiaramente l'intenzione.

Il casting esplicito può essere eseguito principalmente in due modi. Il primo è il C-style cast, simile al linguaggio C, che utilizza la sintassi (tipo)variabile. È breve e veloce da scrivere, ma meno sicuro perché non distingue i vari tipi di cast. Il secondo metodo è il cast in stile C++, come static_cast<tipo>(variabile), introdotto per fornire maggiore sicurezza e chiarezza, poiché rende il cast più evidente e controllato.

C++ permette di effettuare cast anche tra tipi compatibili, ad esempio da char a int, da int a float o viceversa, e perfino tra tipi interi e booleani. Le conversioni possono essere applicate anche all'interno di espressioni matematiche, influenzando il risultato dell'operazione; ad esempio, convertire un intero in double all’interno di una divisione permette di ottenere un valore decimale invece che un arrotondamento per difetto. È importante usare il casting con attenzione, soprattutto quando può comportare perdita di informazioni.

``` cpp +Prodotto.cpp
#include <iostream>
using namespace std;

int main() {
    int a = 7;
    int b = 2;

    // Divisione intera (perde la parte decimale)
    int risultato_intero = a / b;     // vale 3

    // Casting esplicito in stile C (double)
    double risultato_c_style = (double)a / b; // vale 3.5

    // Casting esplicito in stile C++ (static_cast)
    double risultato_cpp_style = static_cast<double>(a) / b; // vale 3.5

    // Conversione implicita
    double d = a;   // d diventa 7.0

    // Casting verso un tipo più piccolo
    double pi = 3.14159;
    int pi_intero = static_cast<int>(pi); // vale 3, perde i decimali

    // Casting tra tipi completamente diversi (char -> int)
    char lettera = 'A';
    int codice_ascii = static_cast<int>(lettera); // vale 65

    // Output
    cout << "Divisione intera: " << risultato_intero << endl;
    cout << "Casting stile C: " << risultato_c_style << endl;
    cout << "Casting stile C++: " << risultato_cpp_style << endl;
    cout << "Conversione implicita: " << d << endl;
    cout << "Casting double -> int: " << pi_intero << endl;
    cout << "Char 'A' in int: " << codice_ascii << endl;

    return 0;
}
```
@LIA.cpp

##  gli operatori di relazione e quelli logici (pag 99)

In C++ gli operatori di relazione e gli operatori logici sono fondamentali per costruire condizioni, confronti e decisioni all’interno delle istruzioni di controllo, come if, while e for.

Gli operatori di relazione confrontano due valori e restituiscono un risultato di tipo bool: true (vero) oppure false (falso). Vengono utilizzati per verificare uguaglianze, disuguaglianze o confronti numerici. Tra questi troviamo == per verificare l’uguaglianza, != per verificare la differenza, > e < per determinare se un valore è maggiore o minore di un altro, e >= e <= per confronti più ampi che includono l’uguaglianza. Questi operatori sono molto usati nei flussi decisionali e permettono di costruire espressioni condizionali anche complesse.

Gli operatori logici, invece, servono per combinare più condizioni booleane e ottenere un unico risultato. L’operatore && (AND logico) restituisce vero solo se entrambe le condizioni sono vere, mentre || (OR logico) restituisce vero se almeno una condizione è vera. L’operatore ! (NOT logico) inverte il valore logico di un’espressione: se era vero diventa falso, se era falso diventa vero. Un aspetto importante è che gli operatori logici in C++ eseguono il cosiddetto short-circuit: nel caso dell’AND, se la prima condizione è falsa, la seconda non viene neppure valutata; per l’OR accade l’opposto, se la prima è vera, la seconda viene ignorata. Questo permette di ottimizzare le condizioni e prevenire valutazioni inutili o pericolose.

Combinando operatori di relazione e operatori logici si possono creare condizioni anche molto articolate, utili per controllare flussi complessi nel programma. È importante ricordare che queste espressioni restituiscono sempre un valore booleano, anche quando i confronti riguardano variabili numeriche o caratteri.

``` cpp +Prodotto.cpp
#include <iostream>
using namespace std;

int main() {
    int a = 10;
    int b = 20;
    int c = 10;

    // Operatori di relazione
    bool uguali = (a == c);       // true
    bool diversi = (a != b);      // true
    bool maggiore = (b > a);      // true
    bool minoreUguale = (a <= c); // true

    // Operatori logici
    bool condizione_and = (a == c) && (b > a);      // true AND true -> true
    bool condizione_or = (a == b) || (b > a);       // false OR true -> true
    bool negazione = !(a == b);                     // !(false) -> true

    // Uso combinato in una condizione
    if ((a == c && b > a) || !(b == c)) {
        cout << "La condizione complessa è vera." << endl;
    } else {
        cout << "La condizione complessa è falsa." << endl;
    }

    // Output dei risultati
    cout << "a == c: " << uguali << endl;
    cout << "a != b: " << diversi << endl;
    cout << "b > a: " << maggiore << endl;
    cout << "a <= c: " << minoreUguale << endl;
    cout << "(a==c && b>a): " << condizione_and << endl;
    cout << "(a==b || b>a): " << condizione_or << endl;
    cout << "!(a==b): " << negazione << endl;

    return 0;
}
```
@LIA.cpp

## le istruzioni di ingresso e di uscita (pag 101)

In C++ le istruzioni di ingresso e di uscita permettono la comunicazione tra il programma e l’utente. Le operazioni di uscita servono per mostrare dati o messaggi sullo schermo, mentre quelle di ingresso consentono di leggere dati digitati dall’utente tramite tastiera. Per usare queste funzionalità è necessario includere la libreria <iostream>, che mette a disposizione gli oggetti cout e cin.

L’istruzione di uscita utilizza l’oggetto cout insieme all’operatore <<, chiamato operatore di inserimento. Questo operatore invia ciò che si trova a destra verso lo stream di uscita. È possibile concatenare più valori o stringhe in un’unica istruzione. Per andare a capo, si può utilizzare endl — che oltre a mandare a capo svuota il buffer — oppure il carattere speciale \n. L’uso di cout è molto frequente per mostrare risultati, messaggi di errore o richieste di input.

Le istruzioni di ingresso invece usano l’oggetto cin assieme all’operatore >>, chiamato operatore di estrazione. Questo operatore legge ciò che l’utente digita e lo memorizza nella variabile posta a destra. L’input viene letto fino al primo spazio, quindi per leggere più parole sarebbe necessario usare funzioni come getline(). Il cin tenta automaticamente di convertire l’input nel tipo della variabile, quindi un dato non compatibile può provocare un errore di input.

È possibile concatenare più letture in un’unica istruzione cin, e spesso si scrivono messaggi con cout prima delle letture per guidare l’utente. La combinazione di input e output permette di realizzare programmi interattivi che elaborano e mostrano risultati in base alle informazioni ricevute.

``` cpp +Prodotto.cpp
#include <iostream>
using namespace std;

int main() {
    int eta;
    double altezza;
    string nome;

    // Messaggi in uscita
    cout << "Inserisci il tuo nome: ";
    
    // Lettura stringa con una sola parola
    cin >> nome;

    cout << "Inserisci la tua eta: ";
    cin >> eta;

    cout << "Inserisci la tua altezza in metri: ";
    cin >> altezza;

    // Uscita dei dati inseriti
    cout << "\n--- RISULTATI ---\n";
    cout << "Nome: " << nome << endl;
    cout << "Eta: " << eta << " anni" << endl;
    cout << "Altezza: " << altezza << " m\n";

    return 0;
}
```
@LIA.cpp

## gli errori nella programmazione + le strutture di alternativa (pag 104-107)
Nel linguaggio C++ gli errori di programmazione rappresentano problemi che possono verificarsi durante lo sviluppo di un programma e possono impedirne il corretto funzionamento. Questi errori si dividono principalmente in tre categorie. Gli errori di compilazione (o di sintassi) avvengono quando non vengono rispettate le regole del linguaggio, come l’omissione di un punto e virgola, l’uso di una variabile non dichiarata o una parentesi mancante. In questo caso il compilatore blocca la compilazione e segnala l’errore, impedendo l’esecuzione del programma.

Gli errori di esecuzione (runtime) si verificano quando il programma, pur compilando correttamente, incontra una situazione non gestibile durante l’esecuzione, come una divisione per zero, l’accesso a memoria non valida o un input non adeguato fornito dall’utente. Questi errori possono provocare l’arresto improvviso del programma.

Infine, gli errori logici sono i più difficili da individuare perché non generano messaggi di errore: il programma funziona e si esegue, ma i risultati ottenuti non sono quelli desiderati. Ciò accade, ad esempio, quando si usa un’operazione sbagliata, si imposta una condizione errata o si applica un algoritmo in modo scorretto.

Per gestire situazioni in cui il programma deve prendere decisioni, C++ utilizza la struttura di alternativa, basata sulle istruzioni if, else if ed else. Queste permettono al programma di eseguire percorsi diversi a seconda delle condizioni valutate. L’istruzione if controlla se una condizione è vera e, in tal caso, esegue un blocco di codice. Se la condizione è falsa, può essere utilizzato else per eseguire istruzioni alternative. Quando occorre gestire più situazioni diverse, si ricorre a else if, che permette di concatenare più condizioni in ordine di verifica.

L’uso corretto delle strutture di alternativa è fondamentale sia per evitare errori di esecuzione sia per correggere errori logici, poiché consente di controllare i dati prima di usarli e di rendere il comportamento del programma più preciso e prevedibile.

``` cpp +Prodotto.cpp
#include <iostream>
using namespace std;

int main() {
    int a, b;

    cout << "Inserisci due numeri: ";
    cin >> a >> b;

    // Struttura di alternativa per evitare errore di esecuzione
    if (b != 0) {
        cout << "Risultato della divisione: " << a / b << endl;
    } else {
        cout << "Errore: impossibile dividere per zero." << endl;
    }

    // Esempio di errore logico (voluto): uso della sottrazione al posto della somma
    int somma = a - b;  // LOGICAMENTE sbagliato
    cout << "Somma (errata a causa di errore logico): " << somma << endl;

    // Esempio di errore di compilazione (scritto come commento)
    // int x = "testo";  // ERRORE: tipo non compatibile con int

    return 0;
}

```
@LIA.cpp

## le ripetizione nel c++ (pag 111-116)
Nel linguaggio C++ le strutture di ripetizione permettono di eseguire un insieme di istruzioni più volte, finché una condizione è soddisfatta o finché viene raggiunto un numero prefissato di iterazioni. Le ripetizioni servono per automatizzare operazioni, evitare codice ripetitivo e gestire sequenze di calcoli o controlli.

La ripetizione precondizionale è quella in cui la condizione viene verificata prima di eseguire il blocco di istruzioni. In C++ questa struttura è rappresentata dal ciclo while. Il corpo del ciclo viene eseguito solo se la condizione iniziale risulta vera: se è falsa sin dall'inizio, il ciclo non viene eseguito nemmeno una volta. Questo tipo di ripetizione è utile quando non si sa in anticipo quante volte sarà necessario ripetere un’operazione.

Un'altra forma di ripetizione è la ripetizione con contatore, rappresentata dal ciclo for. Questa struttura è ideale quando si conosce esattamente il numero di iterazioni da eseguire. Il ciclo for include in un’unica riga l’inizializzazione del contatore, la condizione di continuazione e l’aggiornamento del contatore, rendendolo particolarmente compatto e leggibile.

Oltre a queste, esistono forme generiche di ripetizione, come il ciclo do…while, che garantisce almeno un’esecuzione del blocco prima di controllare la condizione, ma appartiene alle strutture di ripetizione non precondizionali. In generale, l’uso corretto dei cicli consente di controllare il flusso del programma e di gestire operazioni iterative in modo efficiente e organizzato.

``` cpp +Prodotto.cpp
#include <iostream>
using namespace std;

int main() {

    int num;
    int somma = 0;

    cout << "Inserisci numeri positivi (0 per terminare): ";
    cin >> num;

    // RIPETIZIONE PRECONDIZIONALE (while)
    while (num > 0) {     // si ripete finché la condizione è vera
        somma += num;
        cin >> num;
    }

    cout << "Somma dei numeri inseriti: " << somma << endl;

    // RIPETIZIONE CON CONTATORE (for)
    cout << "Conto da 1 a 5 usando un ciclo for: ";
    for (int i = 1; i <= 5; i++) {   // contatore da 1 a 5
        cout << i << " ";
    }

    cout << endl;
    return 0;
}
```
@LIA.cpp

##  la struttura di scelta multipla (pag 119-121)

In C++ lo strumento di scelta multipla, rappresentato dall’istruzione switch, permette di gestire più percorsi alternativi in modo chiaro e compatto, soprattutto quando si devono confrontare più valori di una stessa variabile.

La sintassi generale è:

``` cpp +Somma.cpp
switch (espressione) {
    case valore1:
        // istruzioni se espressione == valore1
        break;
    case valore2:
        // istruzioni se espressione == valore2
        break;
    ...
    default:
        // istruzioni se nessun caso precedente corrisponde
}
```
@LIA.cpp

Funzionamento:

L’espressione dentro switch viene valutata una sola volta.

Il programma confronta il risultato con ciascun case.

Quando trova una corrispondenza, esegue le istruzioni associate fino a incontrare break o la fine del switch.

Il break impedisce l’esecuzione dei casi successivi (fall-through).

Il default è opzionale e viene eseguito se nessun caso corrisponde.

Il switch-case è utile quando si devono gestire scelte tra numeri, caratteri o enumerazioni, rendendo il codice più leggibile rispetto a molteplici if-else if.

``` cpp +Prodotto.cpp
#include <iostream>
using namespace std;

int main() {
    int giorno;

    cout << "Inserisci un numero da 1 a 7: ";
    cin >> giorno;

    switch (giorno) {
        case 1:
            cout << "Lunedi" << endl;
            break;
        case 2:
            cout << "Martedi" << endl;
            break;
        case 3:
            cout << "Mercoledi" << endl;
            break;
        case 4:
            cout << "Giovedi" << endl;
            break;
        case 5:
            cout << "Venerdi" << endl;
            break;
        case 6:
            cout << "Sabato" << endl;
            break;
        case 7:
            cout << "Domenica" << endl;
            break;
        default:
            cout << "Numero non valido!" << endl;
    }

    return 0;
}
```
@LIA.cpp
