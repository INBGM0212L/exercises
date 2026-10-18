# `P104206t` - Váltakozó paritású lista (végjelig olvasás)

## A függvény
Írj egy `has_matching_parity` nevű függvényt, mely visszaadja azt, hogy a paraméterként megkapott lista minden eleme azonos paritású-e, mint az indexe!


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
 | `[1, 1, 1, 1]` | `False` |
 | `[1]` | `False` |
 | `[-1]` | `False` |
 | `[1, 2, 3, 5, 8, 13]` | `False` |
 | `[-1, -2, -3, -5, -8, -13]` | `False` |
 | `[10, 20, 30, 50, 80, 130]` | `False` |
 | `[1, -2, 3, -4, 5, -6]` | `False` |
 | `[1, 2, 1, 2]` | `False` |
 | `[1, -3]` | `False` |


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
False
False
False
False
False
False
False
False
False
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
-4 -89 58 -26 -68 96 -36
-9 -27 -97 30
-84 -80 76 24 -82
-46 21 65 -46 26 41
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
-25 -49 -93 -76 -96 69 16
-4 90 53 42
-48
-39 46 73 33 60 -42 -86
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
False
False
True
False
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
-6 -73 -34 60 87 -6 -65 48 17
91 53 -61 4 -56 34 -10 -82 66
-40 38 50 67 -61 7
9 41 -87 -23 25 -7 55 -75 69
-30 0 81 -76 -17 66 -47 90 31 69
60 59
-50 51 -87 -2 -98 66 -26 -28 70
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
False
False
False
False
False
True
False
```
