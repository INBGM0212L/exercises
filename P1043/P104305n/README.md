# `P104305n` - Lista négyzetgyöke (`n` teszteset)

## A függvény
Írj egy `apply_square_root` nevű függvényt, mely visszaadja azt a listát, melyet úgy kapunk, hogy a `numbers` lista minden elemének meghatározzuk a négyzetgyökét, majd az eredményt `3` tizedesjegyre kerekítjük!


### Paraméterlista
1. `numbers` - az eredeti lista (egy legalább `1`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `1`, legfeljebb `99`)

### Visszaadott érték
* a művelet elvégzésével előálló új lista

### Példák
 | `numbers` | Visszaadott érték |
 | :--- | :-- |
 | `[1, 76, 8]` | `[1.0, 8.718, 2.828]` |
 | `[62, 80, 59, 60]` | `[7.874, 8.944, 7.681, 7.746]` |
 | `[65, 44, 25]` | `[8.062, 6.633, 5.0]` |
 | `[79, 10, 65, 30, 54, 16, 34]` | `[8.888, 3.162, 8.062, 5.477, 7.348, 4.0, 5.831]` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek száma az első sorban szereplő egész érték.
* Minden tesztesetet egy külön sor ír le, melyben a feldolgozandó lista (`numbers`) elemei szerepelnek egy-egy szóközzel elválasztva egymástól.

## Megjegyzés a *C* nyelvű megoldásokhoz
* A bemenet egyetlen sora sem hosszabb `1000` karakternél.
* A függvény `numbers` paramétere az egész számokat tartalmazó tömb kezdőcíme.
* A függvény egy harmadik, `length` nevű (egész típusú) paramétert is megkap, mely a `numbers` tömb méretét tartalmazza.
* A függvény egy dinamikusan foglalt tömb kezdőcímét adja vissza. A tömb végét egy extra, `INT_MIN` értékű elem jelzi.
* A főprogram felszabadítja a tömb mögött álló memóriaterületet.
* A példákban látható értékeket egy *Python* nyelvű megoldás állította elő. Lehetséges hogy a két nyelv kerekítési hibája nem pontosan ugyanaz valós értékeknél.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |
| `test-03` | [`test-03.in`](test-03.in) | [`test-03.out`](test-03.out) |

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
4
1 76 8
62 80 59 60
65 44 25
79 10 65 30 54 16 34
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
1.0 8.718 2.828
7.874 8.944 7.681 7.746
8.062 6.633 5.0
8.888 3.162 8.062 5.477 7.348 4.0 5.831
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
5
62 31
88
38 67 90 62 92 19
73
35 77 9
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
7.874 5.568
9.381
6.164 8.185 9.487 7.874 9.592 4.359
8.544
5.916 8.775 3.0
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
10
22 61 79 48
65 52 44 82 71 61 93 94 55 95
42 18 35
92 74 67 9 18 14 19 92
31 19 29 76 59
80 79 85 42 83 19 77 79
25 20 9 88 62 69 66 74 99 82
15 39 59
84 75 74 36 11 98 71 13
63 40 85
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
4.69 7.81 8.888 6.928
8.062 7.211 6.633 9.055 8.426 7.81 9.644 9.695 7.416 9.747
6.481 4.243 5.916
9.592 8.602 8.185 3.0 4.243 3.742 4.359 9.592
5.568 4.359 5.385 8.718 7.681
8.944 8.888 9.22 6.481 9.11 4.359 8.775 8.888
5.0 4.472 3.0 9.381 7.874 8.307 8.124 8.602 9.95 9.055
3.873 6.245 7.681
9.165 8.66 8.602 6.0 3.317 9.899 8.426 3.606
7.937 6.325 9.22
```
