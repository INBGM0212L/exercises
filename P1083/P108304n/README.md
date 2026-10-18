# `P108304n` - LEGO készletek #1 (`n` teszteset)

## A feladat leírása
Egy játékbolt polcain több különböző témájú és méretű Lego készlet közül válogathatunk. Ezek lehetnek kicsi zacskósak, de akár hatalmas dobozosok is. A megvásárolandó készlet kiválasztása éppen ezért sokszor hatalmas fejtörést okoz.

Ebben a feladatban LEGO készletek adatait kell beolvasnod a standard inputról, rendezni, majd kiírni a standard outputra.

## Formátumok

* A standard bemeneten egy LEGO készlet a következő formátumban szerepel:
    ```
    <termékkód>;<szett_neve>;<téma_neve>;<elemek_száma>
    ```

* A standard kimeneten egy LEGO készlet a következő formátumban szerepel:
    ```
    <szett_neve> (<termékkód>): <elemek_száma> - <téma_neve>
    ```

* A jelölések:
  * `termékkód`: egy negmnegatív egész érték
  * `szett_neve`: egy legfeljebb `30` karakter hosszú, csak angol betűket és szóközöket tartalmazó egyedi sztring
  * `téma_neve`: egy legfeljebb `30` karakter hosszú, csak angol betűket és szóközöket tartalmazó egyedi sztring
  * `elemek_száma`: egy nemnegatív egész érték

A feladat megoldását több függvényre kell bontanod, ezek leírását egyenként, lentebb találod.

## A(z) `LegoSet` típus
Definiáld a `LegoSet` nevű nevesített tuple-t, mely a következő mezőkkel rendelkezik:

* `number`: a készlet kódja (típus: `<class 'int'>`)
* `name`: a készlet neve (típus: `<class 'str'>`)
* `theme`: a téma neve (típus: `<class 'str'>`)
* `pieces`: az elemek száma (típus: `<class 'int'>`)

## A(z) `line_to_lego_set` függvény
Írj egy `line_to_lego_set` nevű függvényt, mely megkapja a bemenet egy sorát, majd visszaadja sorból kinyert adatokkal feltöltött, `LegoSet` *nevesített tuple*-t!

### Paraméterlista

1. a bemenet egy `LegoSet` rekordot leíró sora

### Visszaadott érték

* a `line` paraméternek megfelelő `LegoSet` rekord

### Példák

| `entries` | Visszaadott érték |
| --- | --- |
| `"30356;Hot dog arus;Lego City;43"` | `LegoSet(number=30356, name='Hot dog arus', theme='Lego City', pieces=43)` |
| `"30360;Sarkvideki jegfuresz;Lego City;43"` | `LegoSet(number=30360, name='Sarkvideki jegfuresz', theme='Lego City', pieces=43)` |
| `"30381;Birodalmi TIE Fighter;Lego Star Wars;42"` | `LegoSet(number=30381, name='Birodalmi TIE Fighter', theme='Lego Star Wars', pieces=42)` |
| `"10258;London Bus;Lego Creator Expert;1686"` | `LegoSet(number=10258, name='London Bus', theme='Lego Creator Expert', pieces=1686)` |
| `"10253;Big Ben;Lego Creator Expert;4163"` | `LegoSet(number=10253, name='Big Ben', theme='Lego Creator Expert', pieces=4163)` |

## A(z) `lego_set_to_line` függvény

Írj egy `lego_set_to_line` nevű függvényt, mely megkap egy `LegoSet` rekordot, majd visszaadja a neki megfelelő, kimenetre írható sztringet!

### Paraméterlista

1. `lego_set` - a(z) `LegoSet` típusú rekord

### Visszaadott érték

* az `lego_set` paraméternek megfelelő sztring reprezentáció

### Példák

| `entries` | Visszaadott érték |
| --- | --- |
| `LegoSet(number=10253, name='Big Ben', theme='Lego Creator Expert', pieces=4163)` | `"Big Ben (10253): 4163 - Lego Creator Expert"`
| `LegoSet(number=10258, name='London Bus', theme='Lego Creator Expert', pieces=1686)` | `"London Bus (10258): 1686 - Lego Creator Expert"`
| `LegoSet(number=30356, name='Hot dog arus', theme='Lego City', pieces=43)` | `"Hot dog arus (30356): 43 - Lego City"`
| `LegoSet(number=30360, name='Sarkvideki jegfuresz', theme='Lego City', pieces=43)` | `"Sarkvideki jegfuresz (30360): 43 - Lego City"`
| `LegoSet(number=30381, name='Birodalmi TIE Fighter', theme='Lego Star Wars', pieces=42)` | `"Birodalmi TIE Fighter (30381): 42 - Lego Star Wars"`

## A(z) `sort_lego_sets` függvény

Írj egy `sort_lego_sets` nevű függvényt, mely megkap egy `LegoSet` listát, majd rendezi és visszaadja azt!

### Paraméterlista

1. `lego_sets` - a(z) `LegoSet` elemeket tartalmazó lista

### Visszaadott érték

* a paraméterként megkapott `lego_sets` lista a következő szempontok szerint rendezve:

	1. az elemek száma szerint csökken sorrend
	1. a téma neve szerint növekvő sorrend
	1. a készlet neve szerint növekvő sorrend
	1. a készlet kódja szerint növekvő sorrend

### Példák

| `entries` | Visszaadott érték |
| --- | --- |
| `[LegoSet(number=30356, name='Hot dog arus', theme='Lego City', pieces=43), LegoSet(number=30360, name='Sarkvideki jegfuresz', theme='Lego City', pieces=43), LegoSet(number=30381, name='Birodalmi TIE Fighter', theme='Lego Star Wars', pieces=42), LegoSet(number=10258, name='London Bus', theme='Lego Creator Expert', pieces=1686), LegoSet(number=10253, name='Big Ben', theme='Lego Creator Expert', pieces=4163)]` | `[LegoSet(number=10253, name='Big Ben', theme='Lego Creator Expert', pieces=4163), LegoSet(number=10258, name='London Bus', theme='Lego Creator Expert', pieces=1686), LegoSet(number=30356, name='Hot dog arus', theme='Lego City', pieces=43), LegoSet(number=30360, name='Sarkvideki jegfuresz', theme='Lego City', pieces=43), LegoSet(number=30381, name='Birodalmi TIE Fighter', theme='Lego Star Wars', pieces=42)]` |

## A főprogram

Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemenet sorai egy-egy `LegoSet` pontosvesszőkkel (`;`) elválasztott adatait tartalmazzák.
* A standard bemenet első sora tartalmazza a feldolgozandó sorok számát (`n`).
* Az első sort pontosan `n` darab, a feladat szövegének megfelelő sor követi.
* A beolvasott sorok feldolgozása a következő módon történik:
	1. a(z) `LegoSet` lista előállítása a(z) `line_to_lego_set()` függvény felhasználásával
	1. a(z) `LegoSet` lista rendezése a(z) `sort_lego_sets()` függvénnyel
	1. a(z) `LegoSet` lista kiírása a(z) `lego_set_to_line()` függvény felhasználásával

## Megjegyzés a *C* nyelvű megoldásokhoz

* A rendezéshez a `qsort()` függvényt használd.
* A(z) `lego_set_to_line()` függvény a `qsort()` függvény negyedik paramétereként megadható, összehasonlító függvény.
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
5
30356;Hot dog arus;Lego City;43
30360;Sarkvideki jegfuresz;Lego City;43
30381;Birodalmi TIE Fighter;Lego Star Wars;42
10258;London Bus;Lego Creator Expert;1686
10253;Big Ben;Lego Creator Expert;4163
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
Big Ben (10253): 4163 - Lego Creator Expert
London Bus (10258): 1686 - Lego Creator Expert
Hot dog arus (30356): 43 - Lego City
Sarkvideki jegfuresz (30360): 43 - Lego City
Birodalmi TIE Fighter (30381): 42 - Lego Star Wars
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
15
41707;S;U;4661
9789;B;H;8420
79309;E;N;6695
43246;F;W;4832
62938;G;R;935
28047;B;D;137
94328;F;G;3243
40932;N;N;1772
24165;T;X;1291
77580;O;C;1718
91708;N;U;7367
87367;A;E;8901
99012;T;N;5876
61285;C;T;6345
47251;M;S;7154
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
A (87367): 8901 - E
B (9789): 8420 - H
N (91708): 7367 - U
M (47251): 7154 - S
E (79309): 6695 - N
C (61285): 6345 - T
T (99012): 5876 - N
F (43246): 4832 - W
S (41707): 4661 - U
F (94328): 3243 - G
N (40932): 1772 - N
O (77580): 1718 - C
T (24165): 1291 - X
G (62938): 935 - R
B (28047): 137 - D
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
15
63633;Q;C;180
41131;L;M;3937
58671;Y;Y;958
88334;X;V;8073
30864;S;Z;4873
63345;S;E;1564
51032;S;B;762
61662;D;Y;6956
77916;W;N;5521
93967;R;L;5412
51523;G;Z;1140
71632;Y;F;8502
26389;U;W;1585
4577;U;X;3913
66435;V;C;5675
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
Y (71632): 8502 - F
X (88334): 8073 - V
D (61662): 6956 - Y
V (66435): 5675 - C
W (77916): 5521 - N
R (93967): 5412 - L
S (30864): 4873 - Z
L (41131): 3937 - M
U (4577): 3913 - X
U (26389): 1585 - W
S (63345): 1564 - E
G (51523): 1140 - Z
Y (58671): 958 - Y
S (51032): 762 - B
Q (63633): 180 - C
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
11
43699;G;A;2292
92814;F;A;7492
90651;K;L;8426
76490;Q;F;411
94092;H;G;1208
66960;O;A;3691
48200;A;Z;9413
2683;B;X;5595
19829;J;T;4602
84625;U;M;9515
39028;F;T;3680
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
U (84625): 9515 - M
A (48200): 9413 - Z
K (90651): 8426 - L
F (92814): 7492 - A
B (2683): 5595 - X
J (19829): 4602 - T
O (66960): 3691 - A
F (39028): 3680 - T
G (43699): 2292 - A
H (94092): 1208 - G
Q (76490): 411 - F
```
