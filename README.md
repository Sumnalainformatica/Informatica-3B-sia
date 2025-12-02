<!--
author:   Sumna Begom

email:    sumna.begom@savoiabenincasa.it

version:  0.0.1

language: it

narrator: IT Italian Female

comment:  Quaderno elettronico di Informatica. Classe 3za. Capitolo 4. Il linguaggio C++.

import: https://raw.githubusercontent.com/LiaScript/CodeRunner/master/README.md

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
@LIA.cpp


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

In C++ una variabile è uno spazio di memoria identificato da un nome, all'interno del quale è possibile memorizzare un valore. Prima di poterle utilizzare, le variabili devono sempre essere dichiarate specificando il loro tipo (ad esempio int, double, char). L'assegnazione di un valore a una variabile avviene tramite l'operatore =, che copia il valore presente a destra all'interno della variabile posta a sinistra.



## Assegnazione

### File.cpp - pag. 94

``` c +assegnazione.cpp
// assegnazione.cpp
#include <string>
#include <iostream>
using namespace std;

int main() {
    double raggio = 10;
    double area = raggio * raggio * 3.14;
    int tempo_in_sec = 900;
    int durata_in_minuti = tempo_in_sec / 60;
    double spazio = 1000; // 1 km
    double tempo = 6 * 60; // 6 minuti
    double velocita = spazio / tempo;
    const string cognome = "Rossi";
    string nome("Mario");
    
    cout << cognome << " " << nome << endl;

    return 0;
}
```
@LIA.cpp

## il casting per conversione di tipo (p.97)

la conversione di tipo è l’operazione con cui si trasforma un valore da un tipo di dato a un altro. È molto comune nei programmi, soprattutto quando si usano insieme valori di tipo diverso. A volte la conversione avviene automaticamente: queste sono le conversioni implicite, che il compilatore esegue da solo, ma possono causare perdita di precisione (ad esempio quando si passa da un numero decimale a un intero).

Quando invece è il programmatore a richiedere la trasformazione, si parla di conversioni esplicite o cast. Il cast serve per controllare il tipo del risultato e ottenere valori corretti nei calcoli. Nei linguaggi come il C++ può essere scritto in modi diversi, tra cui la forma moderna con la parola chiave static_cast, usata quando si è certi che la conversione sia sicura.



``` cpp +Prodotto.cpp
#include <iostream>
using namespace std;

int main() {
    int a = 5;
    float b = 3.56;
    a = b;
    cout << a;
   
    return 0;
}
```
@LIA.cpp

##  gli operatori di relazione e quelli logici (pag 99)

operatori di relazione, cioè i simboli che permettono di confrontare due valori (come uguaglianza, maggiore, minore, diverso). Questi confronti producono un risultato booleano: vero oppure falso.

Vengono poi introdotti gli operatori logici, che permettono di combinare più condizioni: la congiunzione (che richiede che entrambe le condizioni siano vere), la disgiunzione (che richiede che almeno una sia vera) e la negazione (che ribalta il valore di una condizione). Questi operatori servono a costruire espressioni più complesse utilizzate nei controlli dei programmi.

``` cpp +Prodotto.cpp
// asssegnazione.cpp
#include <iostream>
using namespace std;

int main() 
{
  int a = 5;
  int b = 2;
  float c = 3.56;
  float p;
  p = a/b + c;
  cout << p;

  return 0;
}
```
@LIA.cpp

## le istruzioni di ingresso e di uscita (pag 101)

In C++ l’input si ottiene dalla tastiera con cin e l’output viene mostrato sullo schermo con cout. Gli operatori dedicati permettono di leggere valori inseriti dall’utente e di visualizzare risultati o messaggi. Per usarli serve includere la libreria dell’I/O. È possibile combinare testo e variabili nell’output e usare caratteri speciali per formattare il messaggio. Altri canali di output, come cerr e clog, sono destinati rispettivamente agli errori e ai messaggi di log. Un esempio mostra come richiedere dati, elaborarli e mostrarne l’esito.

``` cpp +Prodotto.cpp
// parcogiochi.cpp: divisione dei biglietti
#include <iostream>
using namespace std;

int main() {
   // input
int biglietti, ragazzi;
// output
int quota, avanzo;

cout << "Numeri di biglietti e di ragazzi: ";
cin >> biglietti / ragazzi;
avanzo = biglietti % ragazzi;
count << "Ad ogni ragazzo spettano" << quota << "biglietti" << endl;
count << "e ne avanzano" << avanzo << ensl;
    return 0;
}

```
@LIA.cpp

## gli errori nella programmazione + le strutture di alternativa (pag 104-107)
Nel linguaggio C++ possono verificarsi diversi tipi di errori. Gli errori lessicali avvengono quando si usano simboli o parole non riconosciute dal linguaggio, mentre quelli sintattici dipendono dal mancato rispetto delle regole di scrittura, come parentesi mancanti o caratteri fuori posto. Questi errori impediscono al programma di essere compilato e vengono segnalati dal compilatore con un messaggio che indica la riga e il tipo di problema. Gli errori semantici e logici, invece, non bloccano la compilazione, ma portano a risultati sbagliati durante l’esecuzione del programma; per individuarli è necessario osservare il comportamento del programma e controllare che i valori prodotti siano corretti. L’insieme delle attività necessarie per trovare e correggere gli errori prende il nome di debugging.

La selezione nel linguaggio C++ permette al programma di scegliere tra due percorsi diversi in base a una condizione. Se la condizione è vera viene eseguito un insieme di istruzioni, mentre se è falsa viene eseguito un insieme alternativo. Questa struttura consente al programma di prendere decisioni e di comportarsi in modo diverso a seconda dei dati inseriti o delle situazioni che si verificano durante l’esecuzione.

``` cpp +Prodotto.cpp
// Quoziente.cpp: divisione di due numeri
#include <iostream>
using namespace std;

int main() {
    int a, b, q;
    cin >> a >> b;
    q = a / b;
    count << q;
    return 0;
}

```
@LIA.cpp

``` cpp +Prodotto.cpp
// Ordina.cpp: due numeri in ordine crescente
#include <iostream>
using namespace std;
int main() {
// input
int a, b;

cout << "due numeri: ";
cin >> a >> b;
if (a < b) {
cout << a << endl;
cout << b << endl; }
else {
cout << b << endl;
cout << a << endl;}
return 0;}
```
@LIA.cpp

## l'importanza della documentazione e le sequenze (pag 106)
La documentazione in C++ è La documentazione è fondamentale nel lavoro di programmazione perché permette a chiunque, anche a distanza di tempo, di comprendere come è stato progettato e sviluppato un programma. Una buona documentazione aiuta sia nella fase di analisi del problema sia durante la realizzazione del codice, facilitando eventuali modifiche successive e permettendo di mantenere ordine e chiarezza.

Per essere efficace, la documentazione deve utilizzare nomi significativi per variabili e funzioni, descrivere con precisione i dati utilizzati e spiegare la logica seguita nell’algoritmo. È importante anche inserire commenti all’interno del programma per chiarire i passaggi più complessi e verificare periodicamente la coerenza del lavoro svolto. Documentare bene significa anche fornire istruzioni utili all’utente per comprendere il funzionamento del software.

La sequenza è la struttura di base di un programma: le istruzioni vengono eseguite una dopo l’altra nell’ordine in cui sono scritte. Ogni istruzione termina con un punto e virgola ed è racchiusa, insieme alle altre, tra una coppia di parentesi graffe. La sequenza rappresenta quindi il flusso lineare delle operazioni, utile quando il compito da svolgere non richiede scelte o ripetizioni.


``` cpp +Prodotto.cpp
//calcolosconto.cpp: calcolo del prezzo
#include <iostream>
#include <string>
using nomespace std;
const int PERC = 20;
int main ()
{
   //variabili di input-output
   string descrizione;
   float prezzo;
   //variabili di lavoro
   float sconto;

  cout <<"descrizione e prezzo: ";
  cin >> descrizione >> prezzo;
  sconto = prezzo * PERC / 100;
  prezzo = prezzo - sconto;
  cout << descrizione << ":" << prezzo << endl;
 return 0;
}
```
@LIA.cpp



## le ripetizione nel c++ (pag 111-116)
Nel linguaggio C++ le strutture di ripetizione permettono di eseguire un insieme di istruzioni più volte, finché una condizione è soddisfatta o finché viene raggiunto un numero prefissato di iterazioni. Le ripetizioni servono per automatizzare operazioni, evitare codice ripetitivo e gestire sequenze di calcoli o controlli.
``` cpp +Prodotto.cpp
// Elenco1.cpp: elenco di persone
#include <iostream>
#include <string>
using namespace std;

int main ()
{
  //input
  string name;
  int eta;
  int risp;
  //output
  int conta=0;

do{
cout<< "name:";
cin >> name;
cout<< "Eta:" ;
cin >> eta;
if (eta>=18) conta++;
cout << "elenco finito: 0=no, 1=si?";
cin >> risp;
} while (risp ==0);

cout << "i maggiorenni sono "<< conta << endl;
return 0;
}
```
@LIA.cpp

La ripetizione precondizionale è quella in cui la condizione viene verificata prima di eseguire il blocco di istruzioni. In C++ questa struttura è rappresentata dal ciclo while. Il corpo del ciclo viene eseguito solo se la condizione iniziale risulta vera: se è falsa sin dall'inizio, il ciclo non viene eseguito nemmeno una volta. Questo tipo di ripetizione è utile quando non si sa in anticipo quante volte sarà necessario ripetere un'operazione.
``` cpp +Prodotto.cpp
// divisione.cpp: divisione tra interi con sottrazioni successive
#include <iostream>
using namespace std;
int main()
{
//input
int a, b;
//output
int quoz = 0;  //quoziente della divisione tra interi

cout << "due numeri (dividendo e divisore):";
cin >> a >> b;
while (a >= b) {
   a-=b;
   quoz++;
}

cout << "quoziente = " << quoz << endl;
cout << "resto = " a << endl;
return 0;
}
```
@LIA.cpp




Un'altra forma di ripetizione è la ripetizione con contatore, rappresentata dal ciclo for. Questa struttura è ideale quando si conosce esattamente il numero di iterazioni da eseguire. Il ciclo for include in un'unica riga l'inizializzazione del contatore, la condizione di continuazione e l'aggiornamento del contatore, rendendolo particolarmente compatto e leggibile.

``` cpp +Prodotto.cpp
// Massimo.cpp: massimo di n numeri
#include <iostream>
using namespace std;

int main() {
//int
int n;    // numero dei dati inseriti
int dato;   //dato inserito
// output
int max;    // massimo

cout << "quanti sono i dati?"
cin >> n;
for (int i=1; i<=n; i++) {
cout << "inserisci il "<< i <<" . dato:";
cin >> dato;
if (i ==1) max = dato;
if (dato > max) max=dato; }
cout << "il massimo valore e' " << max << endl;
    
    return 0;
}
```
@LIA.cpp

##  la struttura di scelta multipla (pag 119-121)

In C++ lo strumento di scelta multipla, rappresentato dall'istruzione switch, permette di gestire più percorsi alternativi in modo chiaro e compatto, soprattutto quando si devono confrontare più valori di una stessa variabile.

La sintassi generale è:

``` cpp +Somma.cpp
include <iostream>
using namespace std;

int main() {
    int variabile;

    // qui dovresti assegnare un valore a variabile
    // esempio: cin >> variabile;

    switch (variabile) {
        case valore1:
            istruzioni1;
            break;

        case valore2:
            istruzioni2;
            break;

        case valoren:
            istruzionin;
            break;

        default:
            istruzioni;
            break;
    }

    return 0;
}
```
@LIA.cpp

Funzionamento:

L'espressione dentro switch viene valutata una sola volta.

Il programma confronta il risultato con ciascun case.

Quando trova una corrispondenza, esegue le istruzioni associate fino a incontrare break o la fine del switch.

Il break impedisce l'esecuzione dei casi successivi (fall-through).

Il default è opzionale e viene eseguito se nessun caso corrisponde.

Il switch-case è utile quando si devono gestire scelte tra numeri, caratteri o enumerazioni, rendendo il codice più leggibile rispetto a molteplici if-else if.

``` cpp +Prodotto.cpp
// scontoprogressivo.cpp: sconto progressivo sui prodotti
#include <iostream>
using namespace std;

int main() {
    int giorno;
        // int
         float prezzo;     //prezzo del prodotto
         int pezzi;        // pezzi acquistati
       // output
        float omporto;    // importo da pagare
       // lavoro
        int sconto;      // percentuale di sconto

    cout << "pezzi acquistati: ";
    cin >> pezzi;
    cout << "prezzo del prodotto:";
    cin >> prezzo;
    switch (pezzi) {
        case 1:
            cout << "9" << endl;
            break;
        case 2:
            cout << "8" << endl;
            break;
        case 3:
            cout << "7" << endl;
            break;
        case 4:
            cout << "6" << endl;
            break;
        case 5:
            cout << "5" << endl;
            break;
        case 6:
            cout << "4" << endl;
            break;
        case 7:
            cout << "3" << endl;
            break;
        default:
            sconto = 40;
    }
    importo = pezzi * pezzo * (100.0-sconto)/100.0;
   cout << "importo da pagare=" << importo << endl;
    return 0;
}
```
@LIA.cpp
