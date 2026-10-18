# `P104307e` - Lista `n`. hatványa (állományvégjelig olvasás)

## A függvény
Írj egy `apply_nth_pow` nevű függvényt, mely visszaadja azt a listát, melyet úgy kapunk, hogy a `numbers` lista minden elemének az `n`. hatványra emeljük!


### Paraméterlista
1. `numbers` - az eredeti lista (egy legalább `1`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `1`, legfeljebb `99`)
2. `n` - az `n` értéke (egész érték a(z) `[1,10]` intervallumból)

### Visszaadott érték
* a művelet elvégzésével előálló új lista

### Példák
 | `numbers` | `n` | Visszaadott érték |
 | :--- | :--- | :-- |
 | `[33, 21, 53, 43, 21, 52, 6, 63]` | `2` | `[1089, 441, 2809, 1849, 441, 2704, 36, 3969]` |
 | `[43, 64, 50, 33, 3]` | `4` | `[3418801, 16777216, 6250000, 1185921, 81]` |
 | `[2]` | `7` | `[128]` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek végét állományvégjel (`EOF`) jelzi.

## Megjegyzés a *C* nyelvű megoldásokhoz
* A bemenet egyetlen sora sem hosszabb `1000` karakternél.
* A függvény `numbers` paramétere az egész számokat tartalmazó tömb kezdőcíme.
* A függvény egy harmadik, `length` nevű (egész típusú) paramétert is megkap, mely a `numbers` tömb méretét tartalmazza.
* A függvény egy dinamikusan foglalt tömb kezdőcímét adja vissza. A tömb végét egy extra, `INT_MIN` értékű elem jelzi.
* A főprogram felszabadítja a tömb mögött álló memóriaterületet.
* A példákban látható értékeket egy *Python* nyelvű megoldás állította elő. A *C* nyelv típusaival nem ábrázolható az összes példákban szereplő érték.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |
| `test-03` | [`test-03.in`](test-03.in) | [`test-03.out`](test-03.out) |

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
33 21 53 43 21 52 6 63
2
43 64 50 33 3
4
2
7
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
1089 441 2809 1849 441 2704 36 3969
3418801 16777216 6250000 1185921 81
128
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
70 10 25 81 85 36 27 27 93 26
9
93 69 13 30 83 90
7
90 44 39
3
30 40 56 33 64 40 70 10 86
3
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
40353607000000000 1000000000 3814697265625 150094635296999121 231616946283203125 101559956668416 7625597484987 7625597484987 520411082988487293 5429503678976
60170087060757 7446353252589 62748517 21870000000 27136050989627 47829690000000
729000 85184 59319
27000 64000 175616 35937 262144 64000 343000 1000 636056
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
12 58 20 51 83 66 75 2 33
10
20 69 97
3
33 9 68 23 30
9
24 21 24 11 65 59 25 65 73
2
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
61917364224 430804206899405824 10240000000000 119042423827613001 15516041187205853449 1568336880910795776 5631351470947265625 1024 1531578985264449
8000 328509 912673
46411484401953 387420489 31087100296429568 1801152661463 19683000000000
576 441 576 121 4225 3481 625 4225 5329
```
