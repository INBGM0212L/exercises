# `P109603t` - Repülőterek (végjelig olvasás)

## A feladat leírása
Gyakran előfordul, hogy több órát kell csatlakozásra várnunk egy repülőút során. Az ilyen időszak egy átlagos ember számára idegtépő tud lenni, nem úgy egy repülőfotós, avagy planespotter számára. Ők gyakran utaznak csak azért, hogy repülőket fotózzanak, így az utazásuk tervezése során kimondottan keresik azokat a forgalmas reptereket, ahol minél több repülőgépet tudnak megörökíteni egy-egy átszállás során.

Ebben a feladatban repülőterek adatait kell beolvasnod a standard inputról, majd feldolgozni a beolvasott listát.

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

| `line` | Visszaadott érték |
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

| `airport` | Visszaadott érték |
| --- | --- |
| `Airport(name='Zurich Kloten', city='Zurich', runways=3, time=360)` | `"Zurich Kloten (Zurich): 360"`
| `Airport(name='London Heathrow', city='London', runways=2, time=240)` | `"London Heathrow (London): 240"`
| `Airport(name='Istanbul Ataturk', city='Isztambul', runways=3, time=120)` | `"Istanbul Ataturk (Isztambul): 120"`
| `Airport(name='Barcelona El Prat', city='Barcelona', runways=3, time=150)` | `"Barcelona El Prat (Barcelona): 150"`

## A(z) `count_by_runways` függvény

Írj egy `count_by_runways` nevű függvényt, mely visszaadja azt, hogy az `airports` paraméterként megkapott listában hány darab repülőtér rendelkezik a különböző számú futópályákkal!

### Paraméterlista

1. `airports` - a(z) `Airport` elemeket tartalmazó lista (típusa: `list[Airport]`)

### Visszaadott érték

* egy szótár, melynek a kulcsai a futópályák darabszámai, egy-egy értéke pedig az adott darabszámhoz tartozó repülőterek száma (típusa: `dict[int, int]`)


### Példák

| `airports` | Visszaadott érték |
| --- | --- |
| `[Airport(name='Zurich Kloten', city='Zurich', runways=3, time=360), Airport(name='London Heathrow', city='London', runways=2, time=240), Airport(name='Istanbul Ataturk', city='Isztambul', runways=3, time=120), Airport(name='Barcelona El Prat', city='Barcelona', runways=3, time=150)]` | `{'3': 3, '2': 1}` |

## A(z) `read_airports_from_file` függvény

Írj egy `read_airports_from_file` nevű függvényt, mely beolvassa egy szöveges fájlból, majd visszaadja a(z) `Airport` típusú rekordok listáját!

### Paraméterlista

1. `file_name` - annak a fájlnak a neve (elérési útvonala), melyből a(z) `Airport` típusú listát beolvassa a függvény (típusa: `<class 'str'>`)

### Visszaadott érték

* a beolvasott `Airport` rekordok listája (típusa: `list[Airport]`)


### Példa

* A(z) `file_name` paraméter értéke: `"bemenet.txt"`
* A(z) `"bemenet.txt"` szöveges fájl tartalma:
    ```
	Zurich Kloten;Zurich;3;360
	London Heathrow;London;2;240
	Istanbul Ataturk;Isztambul;3;120
	Barcelona El Prat;Barcelona;3;150
    ```

* A függvény által visszaadott lista elemei:
    ```
	Airport(name='Zurich Kloten', city='Zurich', runways=3, time=360)
	Airport(name='London Heathrow', city='London', runways=2, time=240)
	Airport(name='Istanbul Ataturk', city='Isztambul', runways=3, time=120)
	Airport(name='Barcelona El Prat', city='Barcelona', runways=3, time=150)
    ```


## A főprogram

Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A szöveges fájl sorai egy-egy `Airport` pontosvesszőkkel (`;`) elválasztott adatait tartalmazzák.
* A tesztesetek végét a következő sor jelzi (melyet már nem kell feldolgozni): `"END"`.
* A szöveges fájl beolvasása és feldolgozása a következő módon történik:
	* A főprogram a beolvasandó szöveges fájl nevét az első parancssori argumentumként kapja meg.
	1. A(z) főprogram meghívja a(z) `read_airports_from_file()` függvényt, melynek átadja az első parancssori argumentumot.
	1. A(z) `read_airports_from_file()` függvény megnyitja a paraméterként megkapott fájlt, majd a(z) `line_to_airport` függvény felhasználásával beolvassa és visszaadja a(z) `Airport` rekordok listáját.
	1. A(z) `count_by_runways()` függvény meghívása.
	1. A visszakapott szótár bejegyzéseinek kiírása. Minden bejegyzés egy külön, `<kulcs>: <érték>` formátumú sorba kerüljön, ahol a `kulcs` a szótár egy kulcsa, az `érték` pedig a kulcshoz tartozó érték.

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
END
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
3: 3
2: 1
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
END
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
1: 2
4: 3
2: 4
3: 2
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
END
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
2: 5
4: 2
3: 2
1: 1
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
END
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
4: 6
3: 5
2: 5
1: 2
```
