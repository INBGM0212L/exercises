# `P108303e` - Repülőterek (állományvégjelig olvasás)

## A feladat leírása
Gyakran előfordul, hogy több órát kell csatlakozásra várnunk egy repülőút során. Az ilyen időszak egy átlagos ember számára idegtépő tud lenni, nem úgy egy repülőfotós, avagy planespotter számára. Ők gyakran utaznak csak azért, hogy repülőket fotózzanak, így az utazásuk tervezése során kimondottan keresik azokat a forgalmas reptereket, ahol minél több repülőgépet tudnak megörökíteni egy-egy átszállás során.

Ebben a feladatban repülőterek adatait kell beolvasnod a standard inputról, rendezni, majd kiírni a standard outputra.

## Formátumok

* A standard bemeneten egy repülőtér a következő formátumban szerepel:
    ```
    <reptér_neve>;<város>;<futópályák_száma>;<átszállás_hossza>
    ```

* A standard kimeneten egy repülőtér a következő formátumban szerepel:
    ```
    <repülőtér_neve> (<város>): <átszállás_hossza>
    ```

* A jelölések:
  * `repülőtér_neve`: egy legfeljebb `30` karakter hosszú, csak angol betűket és szóközöket tartalmazó egyedi sztring
  * `város`: egy legfeljebb `30` karakter hosszú, csak angol betűket és szóközöket tartalmazó egyedi sztring
  * `futópályák_száma`: egy nemnegatív egész érték
  * `átszállás_hossza`: egy nemnegatív egész érték

A feladat megoldását több függvényre kell bontanod, ezek leírását egyenként, lentebb találod.

## A(z) `Airport` típus
Definiáld a `Airport` nevű nevesített tuple-t, mely a következő mezőkkel rendelkezik:

* `name`: a repülőtér neve (típus: `<class 'str'>`)
* `city`: a város neve (típus: `<class 'str'>`)
* `runways`: a futópályák száma (típus: `<class 'int'>`)
* `time`: az átszállási idő (típus: `<class 'int'>`)

## A(z) `line_to_airport` függvény
Írj egy `line_to_airport` nevű függvényt, mely megkapja a bemenet egy sorát, majd visszaadja sorból kinyert adatokkal feltöltött, `Airport` *nevesített tuple*-t!

### Paraméterlista

1. a bemenet egy `Airport` rekordot leíró sora

### Visszaadott érték

* a `line` paraméternek megfelelő `Airport` rekord

### Példák

| `entries` | Visszaadott érték |
| --- | --- |
| `"Zurich Kloten;Zurich;3;360"` | `Airport(name='Zurich Kloten', city='Zurich', runways=3, time=360)` |
| `"London Heathrow;London;2;240"` | `Airport(name='London Heathrow', city='London', runways=2, time=240)` |
| `"Istanbul Ataturk;Isztambul;3;120"` | `Airport(name='Istanbul Ataturk', city='Isztambul', runways=3, time=120)` |
| `"Barcelona El Prat;Barcelona;3;150"` | `Airport(name='Barcelona El Prat', city='Barcelona', runways=3, time=150)` |

## A(z) `airport_to_line` függvény

Írj egy `airport_to_line` nevű függvényt, mely megkap egy `Airport` rekordot, majd visszaadja a neki megfelelő, kimenetre írható sztringet!

### Paraméterlista

1. `airport` - a(z) `Airport` típusú rekord

### Visszaadott érték

* az `airport` paraméternek megfelelő sztring reprezentáció

### Példák

| `entries` | Visszaadott érték |
| --- | --- |
| `Airport(name='Zurich Kloten', city='Zurich', runways=3, time=360)` | `"Zurich Kloten (Zurich): 360"`
| `Airport(name='Barcelona El Prat', city='Barcelona', runways=3, time=150)` | `"Barcelona El Prat (Barcelona): 150"`
| `Airport(name='Istanbul Ataturk', city='Isztambul', runways=3, time=120)` | `"Istanbul Ataturk (Isztambul): 120"`
| `Airport(name='London Heathrow', city='London', runways=2, time=240)` | `"London Heathrow (London): 240"`

## A(z) `sort_airports` függvény

Írj egy `sort_airports` nevű függvényt, mely megkap egy `Airport` listát, majd rendezi és visszaadja azt!

### Paraméterlista

1. `airports` - a(z) `Airport` elemeket tartalmazó lista

### Visszaadott érték

* a paraméterként megkapott `airports` lista a következő szempontok szerint rendezve:

	1. a futópályák száma szerint csökkenő sorrend
	1. az átszállási idő szerint csökkenő sorrend
	1. a repülőtér neve szerint növekvő sorrend

### Példák

| `entries` | Visszaadott érték |
| --- | --- |
| `[Airport(name='Zurich Kloten', city='Zurich', runways=3, time=360), Airport(name='London Heathrow', city='London', runways=2, time=240), Airport(name='Istanbul Ataturk', city='Isztambul', runways=3, time=120), Airport(name='Barcelona El Prat', city='Barcelona', runways=3, time=150)]` | `[Airport(name='Zurich Kloten', city='Zurich', runways=3, time=360), Airport(name='Barcelona El Prat', city='Barcelona', runways=3, time=150), Airport(name='Istanbul Ataturk', city='Isztambul', runways=3, time=120), Airport(name='London Heathrow', city='London', runways=2, time=240)]` |

## A főprogram

Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemenet sorai egy-egy `Airport` pontosvesszőkkel (`;`) elválasztott adatait tartalmazzák.
* A tesztesetek végét állományvégjel (`EOF`) jelzi.
* A beolvasott sorok feldolgozása a következő módon történik:
	1. a(z) `Airport` lista előállítása a(z) `line_to_airport()` függvény felhasználásával
	1. a(z) `Airport` lista rendezése a(z) `sort_airports()` függvénnyel
	1. a(z) `Airport` lista kiírása a(z) `airport_to_line()` függvény felhasználásával

## Megjegyzés a *C* nyelvű megoldásokhoz

* A rendezéshez a `qsort()` függvényt használd.
* A(z) `airport_to_line()` függvény a `qsort()` függvény negyedik paramétereként megadható, összehasonlító függvény.
* Minden dinamikusan foglalt területet fel kell szabadítani.
* A bemenet egyik sora sem hosszabb `1000` karakternél.
* A bemeneten legfeljebb `20` rekordot leíró sorra kell számítani.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-00` | [`test-00.in`](test-00.in) | [`test-00.out`](test-00.out) |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |
| `test-03` | [`test-03.in`](test-03.in) | [`test-03.out`](test-03.out) |

### `test-00`

#### Standard bemenet ([`test-00.in`](test-00.in))

```
Zurich Kloten;Zurich;3;360
London Heathrow;London;2;240
Istanbul Ataturk;Isztambul;3;120
Barcelona El Prat;Barcelona;3;150
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
Zurich Kloten (Zurich): 360
Barcelona El Prat (Barcelona): 150
Istanbul Ataturk (Isztambul): 120
London Heathrow (London): 240
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
E;V;1;170
K;C;4;97
C;T;2;55
A;F;4;278
G;V;2;74
B;O;2;148
F;H;3;164
D;J;1;129
H;I;2;83
J;B;3;135
I;R;4;130
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
A (F): 278
I (R): 130
K (C): 97
F (H): 164
J (B): 135
B (O): 148
H (I): 83
G (V): 74
C (T): 55
E (V): 170
D (J): 129
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
H;F;2;176
E;C;2;192
I;H;2;189
C;U;2;161
A;K;4;134
B;T;3;178
D;H;2;115
J;M;3;284
F;X;1;198
G;V;4;269
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
G (V): 269
A (K): 134
J (M): 284
B (T): 178
E (C): 192
I (H): 189
H (F): 176
C (U): 161
D (H): 115
F (X): 198
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
H;U;4;177
B;F;3;185
J;D;3;191
L;Y;4;162
D;L;2;185
G;T;1;93
E;Y;4;265
A;M;2;290
F;S;4;231
P;D;3;138
N;V;2;203
I;H;1;152
M;K;3;268
C;R;4;187
R;K;4;85
Q;F;3;264
O;H;2;189
K;M;2;252
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
E (Y): 265
F (S): 231
C (R): 187
H (U): 177
L (Y): 162
R (K): 85
M (K): 268
Q (F): 264
J (D): 191
B (F): 185
P (D): 138
A (M): 290
K (M): 252
N (V): 203
O (H): 189
D (L): 185
I (H): 152
G (T): 93
```
