# `P104204t` - Monoton csökkenő lista (végjelig olvasás)

## A függvény
Írj egy `is_monotone_decreasing` nevű függvényt, mely visszaadja azt, hogy a paraméterként megkapott lista elemei monoton csökkenő sorozatot alkotnak-e!


### Paraméterlista
1. `numbers` - az ellenőrizendő lista (egy legalább `1`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `-99`, legfeljebb `99`)

### Visszaadott érték
* az ellenőrzés eredménye (`True`, ha a lista megfelel a feltételnek, `False`, ha nem)

### Példák
 | `numbers` | Visszaadott érték |
 | :--- | :-- |
 | `[1, 2, 3, 4, 5, 6]` | `False` |
 | `[6, 5, 4, 3, 2, 1]` | `True` |
 | `[1, 2, 3, 2, 1]` | `False` |
 | `[1, 1, 1, 1]` | `True` |
 | `[1]` | `True` |
 | `[-1]` | `True` |
 | `[1, 2, 3, 5, 8, 13]` | `False` |
 | `[-1, -2, -3, -5, -8, -13]` | `True` |
 | `[10, 20, 30, 50, 80, 130]` | `False` |
 | `[1, -2, 3, -4, 5, -6]` | `False` |
 | `[1, 2, 1, 2]` | `False` |
 | `[1, -3]` | `True` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek végét egy üres sor (`""`) jelzi (melyet már nem kell feldolgozni).
* Minden tesztesetet egy külön sor ír le, melyben a feldolgozandó lista (`numbers`) elemei szerepelnek egy-egy szóközzel elválasztva egymástól.

## Megjegyzés a *C* nyelvű megoldásokhoz
* A bemenet egyetlen sora sem hosszabb `1000` karakternél.
* A függvény `numbers` paramétere az egész számokat tartalmazó tömb kezdőcíme.
* A függvény egy második, `length` nevű (egész típusú) paramétert is megkap, mely a `numbers` tömb méretét tartalmazza.
* Az igaz értéket az `1`, míg a hamis értéket a `0` egész literálok jelölik.

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
1 2 3 4 5 6
6 5 4 3 2 1
1 2 3 2 1
1 1 1 1
1
-1
1 2 3 5 8 13
-1 -2 -3 -5 -8 -13
10 20 30 50 80 130
1 -2 3 -4 5 -6
1 2 1 2
1 -3
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
False
True
False
True
True
True
False
True
False
False
False
True
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
-81 29 58 -50 11 -96 -25 48 47 20
23 90
59 -60 -96 -99 -96 96 -73 -1 -74
-93 -41 -29 -14 81 -15 -67
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
False
False
False
False
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
-42 -18 18 -20 79 -83 64 37 -27
-58 32 -66 13
-89 -88 -36 -28 77 -17 -97 -67 -88 7
-62 19 -36 -37 -66 68 54 -74 -68
18 43
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
False
False
False
False
False
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
73 -96 93 65
31 57 -25 -15 54
-84
-56 -3 22 -14 -93 56 -96 -46
10 -46 -3 97 -19
41 -92 62 60
-21 -82 -67 -72
-70
63 58 -6 53 40 -65
-51 59 44 -51 52 89 44 18
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
False
False
True
False
False
False
False
True
False
False
```
