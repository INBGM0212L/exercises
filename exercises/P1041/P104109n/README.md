# `P104109n` - Lokális maximumhelyek száma (`n` teszteset)

## A függvény
Írj egy `count_of_local_maximums` nevű függvényt, mely visszaadja azt, hogy a paraméterként megkapott listában hány elem nagyobb mindkét szomszédjánál!


### Paraméterlista
1. `numbers` - a feldolgozandó lista (egy legalább `1`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `-99`, legfeljebb `99`)

### Visszaadott érték
* a feltételnek megfelelő elemek száma

### Példák
 | `numbers` | Visszaadott érték |
 | :--- | :-- |
 | `[36, -17, 77, -15, -23, -73, 71, -16, -27]` | `2` |
 | `[19, -79, -85]` | `0` |
 | `[61, 62, -62, -32]` | `1` |
 | `[-3, -68]` | `0` |
 | `[-15, -11, 9, 61, 41, -16, 86, 24, -84]` | `2` |
 | `[36, 27, -44, -93, 54]` | `0` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek száma az első sorban szereplő egész érték.
* Minden tesztesetet egy külön sor ír le, melyben a feldolgozandó lista (`numbers`) elemei szerepelnek egy-egy szóközzel elválasztva egymástól.

## Megjegyzés a *C* nyelvű megoldásokhoz
* A bemenet egyetlen sora sem hosszabb `1000` karakternél.
* A függvény `numbers` paramétere az egész számokat tartalmazó tömb kezdőcíme.
* A függvény egy második, `length` nevű (egész típusú) paramétert is megkap, mely a `numbers` tömb méretét tartalmazza.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |
| `test-03` | [`test-03.in`](test-03.in) | [`test-03.out`](test-03.out) |

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
6
36 -17 77 -15 -23 -73 71 -16 -27
19 -79 -85
61 62 -62 -32
-3 -68
-15 -11 9 61 41 -16 86 24 -84
36 27 -44 -93 54
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
2
0
1
0
2
0
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
6
91
-6 91 -29 77 47 -98 -25 -80
-14 45 60
-77 12 60 60 -63 6
92 37 -96 94 -61 -94 85 -25
87 38
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
0
3
0
0
2
0
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
5
-23 49 39 -30 -30 71 10 -34
-73 52 -68 -97
25
68 -84
-22 -83 35 48 67
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
2
1
0
0
0
```
