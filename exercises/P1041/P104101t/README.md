# `P104101t` - Páratlan elemek száma (végjelig olvasás)

## A függvény
Írj egy `count_of_odds` nevű függvényt, mely visszaadja azt, hogy a paraméterként megkapott lista elemei közül mennyi páratlan szám!


### Paraméterlista
1. `numbers` - a feldolgozandó lista (egy legalább `1`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `-99`, legfeljebb `99`)

### Visszaadott érték
* a feltételnek megfelelő elemek száma

### Példák
 | `numbers` | Visszaadott érték |
 | :--- | :-- |
 | `[-58, 21, 50, 92, 62]` | `1` |
 | `[-52, -30, 29, -19, -84, 8, 31, -67]` | `4` |
 | `[70, 47, -35, -89, -80]` | `3` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek végét egy üres sor (`""`) jelzi (melyet már nem kell feldolgozni).
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
-58 21 50 92 62
-52 -30 29 -19 -84 8 31 -67
70 47 -35 -89 -80
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
1
4
3
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
88 95 -43 84 2 -9 -42 70 72 -96
-7 74
-63 -30 60 69 -24 36
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
3
1
2
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
-15 -98 32 -52 -17 29 45 85 -41
22 35 -70 89 0 -76
79 -3 -12 -67 -3 -72
4 -22 -39 2 43 85 -46
-53 97
-79 -95
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
6
2
4
3
2
2
```
