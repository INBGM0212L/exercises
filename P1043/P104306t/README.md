# `P104306t` - Lista `n`. gyöke (végjelig olvasás)

## A függvény
Írj egy `apply_nth_root` nevű függvényt, mely visszaadja azt a listát, melyet úgy kapunk, hogy a `numbers` lista minden elemének meghatározzuk az `n`. gyökét, majd az eredményt három tizedesjegyre kerekítjük!


### Paraméterlista
1. `numbers` - az eredeti lista (egy legalább `1`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `1`, legfeljebb `99`)
2. `n` - az `n` értéke (egész érték a(z) `[1,10]` intervallumból)

### Visszaadott érték
* a művelet elvégzésével előálló új lista

### Példák
 | `numbers` | `n` | Visszaadott érték |
 | :--- | :--- | :-- |
 | `[70, 96, 88, 19]` | `8` | `[1.701, 1.769, 1.75, 1.445]` |
 | `[64, 27, 27, 29, 99, 84, 70, 85, 59]` | `2` | `[8.0, 5.196, 5.196, 5.385, 9.95, 9.165, 8.367, 9.22, 7.681]` |
 | `[36]` | `4` | `[2.449]` |
 | `[91, 48, 53, 74, 53, 94, 15, 68]` | `5` | `[2.465, 2.169, 2.212, 2.365, 2.212, 2.481, 1.719, 2.325]` |
 | `[80, 23, 34, 89]` | `7` | `[1.87, 1.565, 1.655, 1.899]` |
 | `[53]` | `3` | `[3.756]` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek végét a következő sor jelzi (melyet már nem kell feldolgozni): `"0"`

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
70 96 88 19
8
64 27 27 29 99 84 70 85 59
2
36
4
91 48 53 74 53 94 15 68
5
80 23 34 89
7
53
3
0
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
1.701 1.769 1.75 1.445
8.0 5.196 5.196 5.385 9.95 9.165 8.367 9.22 7.681
2.449
2.465 2.169 2.212 2.365 2.212 2.481 1.719 2.325
1.87 1.565 1.655 1.899
3.756
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
92 70 40 39 98 21 35 9 38
2
45 61 49 82 54 59 29
10
58 96 69 76 1 70 88 22 10 97
1
15
6
55 26 13
6
82 8 8 31 22 46 59
2
37 26
5
32 9 8 43 69 12 20 32 9 41
1
31 92 99 61
2
0
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
9.592 8.367 6.325 6.245 9.899 4.583 5.916 3.0 6.164
1.463 1.508 1.476 1.554 1.49 1.503 1.4
58.0 96.0 69.0 76.0 1.0 70.0 88.0 22.0 10.0 97.0
1.57
1.95 1.721 1.533
9.055 2.828 2.828 5.568 4.69 6.782 7.681
2.059 1.919
32.0 9.0 8.0 43.0 69.0 12.0 20.0 32.0 9.0 41.0
5.568 9.592 9.95 7.81
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
71 98 88 78 16
9
93 82 43 92
7
2 97
7
55 44 60 98 68 34 80 88
7
24 5 11 59 49 20 73
3
78 86 97 21 95 82 97 81 29 71
4
0
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
1.606 1.664 1.645 1.623 1.361
1.911 1.877 1.711 1.908
1.104 1.922
1.773 1.717 1.795 1.925 1.827 1.655 1.87 1.896
2.884 1.71 2.224 3.893 3.659 2.714 4.179
2.972 3.045 3.138 2.141 3.122 3.009 3.138 3.0 2.321 2.903
```
