# `P108305n` - LEGO készletek #2 (`n` teszteset)

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
| `LegoSet(number=30356, name='Hot dog arus', theme='Lego City', pieces=43)` | `"Hot dog arus (30356): 43 - Lego City"`
| `LegoSet(number=30360, name='Sarkvideki jegfuresz', theme='Lego City', pieces=43)` | `"Sarkvideki jegfuresz (30360): 43 - Lego City"`
| `LegoSet(number=10253, name='Big Ben', theme='Lego Creator Expert', pieces=4163)` | `"Big Ben (10253): 4163 - Lego Creator Expert"`
| `LegoSet(number=10258, name='London Bus', theme='Lego Creator Expert', pieces=1686)` | `"London Bus (10258): 1686 - Lego Creator Expert"`
| `LegoSet(number=30381, name='Birodalmi TIE Fighter', theme='Lego Star Wars', pieces=42)` | `"Birodalmi TIE Fighter (30381): 42 - Lego Star Wars"`

## A(z) `sort_lego_sets` függvény

Írj egy `sort_lego_sets` nevű függvényt, mely megkap egy `LegoSet` listát, majd rendezi és visszaadja azt!

### Paraméterlista

1. `lego_sets` - a(z) `LegoSet` elemeket tartalmazó lista

### Visszaadott érték

* a paraméterként megkapott `lego_sets` lista a következő szempontok szerint rendezve:

	1. a téma neve szerint növekvő sorrend
	1. a készlet neve szerint növekvő sorrend
	1. a készlet kódja szerint növekvő sorrend

### Példák

| `entries` | Visszaadott érték |
| --- | --- |
| `[LegoSet(number=30356, name='Hot dog arus', theme='Lego City', pieces=43), LegoSet(number=30360, name='Sarkvideki jegfuresz', theme='Lego City', pieces=43), LegoSet(number=30381, name='Birodalmi TIE Fighter', theme='Lego Star Wars', pieces=42), LegoSet(number=10258, name='London Bus', theme='Lego Creator Expert', pieces=1686), LegoSet(number=10253, name='Big Ben', theme='Lego Creator Expert', pieces=4163)]` | `[LegoSet(number=30356, name='Hot dog arus', theme='Lego City', pieces=43), LegoSet(number=30360, name='Sarkvideki jegfuresz', theme='Lego City', pieces=43), LegoSet(number=10253, name='Big Ben', theme='Lego Creator Expert', pieces=4163), LegoSet(number=10258, name='London Bus', theme='Lego Creator Expert', pieces=1686), LegoSet(number=30381, name='Birodalmi TIE Fighter', theme='Lego Star Wars', pieces=42)]` |

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
Hot dog arus (30356): 43 - Lego City
Sarkvideki jegfuresz (30360): 43 - Lego City
Big Ben (10253): 4163 - Lego Creator Expert
London Bus (10258): 1686 - Lego Creator Expert
Birodalmi TIE Fighter (30381): 42 - Lego Star Wars
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
10
14558;D;Q;3405
18930;I;Y;3894
65661;Y;P;8429
23724;J;B;7476
50558;W;J;8186
11909;A;U;9646
28721;M;V;4555
31196;C;X;1825
87058;N;S;8293
1756;T;U;6888
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
J (23724): 7476 - B
W (50558): 8186 - J
Y (65661): 8429 - P
D (14558): 3405 - Q
N (87058): 8293 - S
A (11909): 9646 - U
T (1756): 6888 - U
M (28721): 4555 - V
C (31196): 1825 - X
I (18930): 3894 - Y
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
20
84423;P;H;6750
32813;T;Q;5683
85508;X;X;3420
24203;Z;V;4603
81416;K;E;3199
24800;L;P;3998
35584;C;O;4757
40881;P;Z;3976
89151;B;M;1457
92471;O;C;2395
17795;W;C;3432
52364;N;N;6497
30823;O;I;9653
95963;O;A;9556
69175;K;U;847
65018;A;Z;6629
89952;Z;R;9513
79818;L;O;4600
1010;P;Y;4218
3993;F;Q;8075
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
O (95963): 9556 - A
O (92471): 2395 - C
W (17795): 3432 - C
K (81416): 3199 - E
P (84423): 6750 - H
O (30823): 9653 - I
B (89151): 1457 - M
N (52364): 6497 - N
C (35584): 4757 - O
L (79818): 4600 - O
L (24800): 3998 - P
F (3993): 8075 - Q
T (32813): 5683 - Q
Z (89952): 9513 - R
K (69175): 847 - U
Z (24203): 4603 - V
X (85508): 3420 - X
P (1010): 4218 - Y
A (65018): 6629 - Z
P (40881): 3976 - Z
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
15
43031;Z;G;4736
17666;X;I;5687
81811;A;U;92
63656;B;X;4505
45020;R;R;7628
99122;P;T;3220
57068;K;E;8532
43502;W;K;341
35459;U;X;1464
38280;S;T;618
99412;L;D;9118
33503;U;G;510
99380;O;D;9097
21297;B;W;8502
71679;M;O;7542
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
L (99412): 9118 - D
O (99380): 9097 - D
K (57068): 8532 - E
U (33503): 510 - G
Z (43031): 4736 - G
X (17666): 5687 - I
W (43502): 341 - K
M (71679): 7542 - O
R (45020): 7628 - R
P (99122): 3220 - T
S (38280): 618 - T
A (81811): 92 - U
B (21297): 8502 - W
B (63656): 4505 - X
U (35459): 1464 - X
```
