# `P104202t` - Monoton növekvő lista (végjelig olvasás)

## A függvény
Írj egy `is_monotone_increasing` nevű függvényt, mely visszaadja azt, hogy a paraméterként megkapott lista elemei monoton nökvekvő sorozatot alkotnak-e!


### Paraméterlista
1. `numbers` - az ellenőrizendő lista (egy legalább `1`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `-99`, legfeljebb `99`)

### Visszaadott érték
* az ellenőrzés eredménye (`True`, ha a lista megfelel a feltételnek, `False`, ha nem)

### Példák
 | `numbers` | Visszaadott érték |
 | :--- | :-- |
 | `[1, 2, 3, 4, 5, 6]` | `True` |
 | `[6, 5, 4, 3, 2, 1]` | `False` |
 | `[1, 2, 3, 2, 1]` | `False` |
 | `[1, 1, 1, 1]` | `True` |
 | `[1]` | `True` |
 | `[-1]` | `True` |
 | `[1, 2, 3, 5, 8, 13]` | `True` |
 | `[-1, -2, -3, -5, -8, -13]` | `False` |
 | `[10, 20, 30, 50, 80, 130]` | `True` |
 | `[1, -2, 3, -4, 5, -6]` | `False` |
 | `[1, 2, 1, 2]` | `False` |
 | `[1, -3]` | `False` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek végét egy üres sor (`""`) jelzi (melyet már nem kell feldolgozni).
* Minden tesztesetet egy külön sor ír le, melyben a feldolgozandó lista (`numbers`) elemei szerepelnek egy-egy szóközzel elválasztva egymástól.

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
True
False
False
True
True
True
True
False
True
False
False
False
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
-16 49 -15 74 -1
22 -50 -98
3
17 58 70 13 -11 79 -44 -48 -32
-85 66 19
-30 77
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
False
False
True
False
False
True
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
21 -59 -30 64 27
44 29 15 43
-16
-3
-78 -11
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
False
False
True
True
True
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
-3 7 -17 -92 65 40 -34 -8
-9 -42 -75 13 -88 41 -8 29 36 89
70 83 42 -2 39 -22 -17 -83
57 93 -19 -70 83 71 -37
-83 3 -56 -81 24 98 -57 -42 -77 54
27 96 -32 86 -76 -31
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
False
False
False
False
False
False
```
