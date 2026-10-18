# `P104104e` - Négyzet elemek száma (állományvégjelig olvasás)

## A függvény
Írj egy `count_of_squares` nevű függvényt, mely visszaadja azt, hogy a paraméterként megkapott lista elemei közül mennyi négyzetszám!


### Paraméterlista
1. `numbers` - a feldolgozandó lista (egy legalább `1`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `1`, legfeljebb `99`)

### Visszaadott érték
* a feltételnek megfelelő elemek száma

### Példák
 | `numbers` | Visszaadott érték |
 | :--- | :-- |
 | `[63, 64, 14, 6, 10, 6, 39, 37, 71]` | `1` |
 | `[71, 29]` | `0` |
 | `[82, 65, 71, 79, 46, 88]` | `0` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek végét állományvégjel (`EOF`) jelzi.
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
63 64 14 6 10 6 39 37 71
71 29
82 65 71 79 46 88
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
1
0
0
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
78 58
30 86 40 74 70
44 24 66 62 88 45 6 38
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
0
0
0
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
46 69 74 46 29 42 40 70
67 93 82 84 45 94 25
47 47 7
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
0
1
0
```
