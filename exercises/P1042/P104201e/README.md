# `P104201e` - Palindrom lista (állományvégjelig olvasás)

## A függvény
Írj egy `is_palindrome` nevű függvényt, mely visszaadja azt, hogy a paraméterként megkapott lista palindrom-e!


### Paraméterlista
1. `numbers` - az ellenőrizendő lista (egy legalább `1`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `-99`, legfeljebb `99`)

### Visszaadott érték
* az ellenőrzés eredménye (`True`, ha a lista megfelel a feltételnek, `False`, ha nem)

### Példák
 | `numbers` | Visszaadott érték |
 | :--- | :-- |
 | `[1, 2, 3, 4, 5, 6]` | `False` |
 | `[6, 5, 4, 3, 2, 1]` | `False` |
 | `[1, 2, 3, 2, 1]` | `True` |
 | `[1, 1, 1, 1]` | `True` |
 | `[1]` | `True` |
 | `[-1]` | `True` |
 | `[1, 2, 3, 5, 8, 13]` | `False` |
 | `[-1, -2, -3, -5, -8, -13]` | `False` |
 | `[10, 20, 30, 50, 80, 130]` | `False` |
 | `[1, -2, 3, -4, 5, -6]` | `False` |
 | `[1, 2, 1, 2]` | `False` |
 | `[1, -3]` | `False` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek végét állományvégjel (`EOF`) jelzi.
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
False
True
True
True
True
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
-95 59 -29 55 -43 -39 6 91 88 -3
-69 42 20 57
-66
60 4 13 -22
34 -78
-85 -39 99 93
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
False
False
True
False
False
False
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
-41 6 63 -27 47
75
17 26 -78 89
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
False
True
False
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
-75 5 -44 0 -35 -96 -66 -81 74
67
-9 56 -71 67 -25 -51 -31 -5 34 86
40 -47 9 -15 52
-60 -36 72
-2 -3 62 -11
-74 89 5 -94 -31 84 -19 29 -19 -31
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
False
True
False
False
False
False
False
```
