# `P104208n` - Fibonacci lista (`n` teszteset)

## A függvény
Írj egy `is_fibonacci` nevű függvényt, mely visszaadja azt, hogy a paraméterként megkapott lista elemei Fibonacci sorozatot alkotnak-e (azaz mindegyik elem az őt megelőző két elem összege)!


### Paraméterlista
1. `numbers` - az ellenőrizendő lista (egy legalább `3`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `-99`, legfeljebb `99`)

### Visszaadott érték
* az ellenőrzés eredménye (`True`, ha a lista megfelel a feltételnek, `False`, ha nem)

### Példák
 | `numbers` | Visszaadott érték |
 | :--- | :-- |
 | `[1, 2, 3, 4, 5, 6]` | `False` |
 | `[6, 5, 4, 3, 2, 1]` | `False` |
 | `[1, 2, 3, 2, 1]` | `False` |
 | `[1, 1, 1, 1]` | `False` |
 | `[1]` | `True` |
 | `[-1]` | `True` |
 | `[1, 2, 3, 5, 8, 13]` | `True` |
 | `[-1, -2, -3, -5, -8, -13]` | `True` |
 | `[10, 20, 30, 50, 80, 130]` | `True` |
 | `[1, -2, 3, -4, 5, -6]` | `False` |
 | `[1, 2, 1, 2]` | `False` |
 | `[1, -3]` | `True` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek száma az első sorban szereplő egész érték.
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
12
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
False
False
True
True
True
True
True
False
False
True
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
4
52 55 -17 -9
-19 -73 14 45 3 -46 -13
-48 13 49 68 -94
19 -59 53 93
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
10
45 -51 -95
-22 56 63 -59 -4 -17 -39 20 -94 46
66 74 -32 83 62
-66 16 22 -45 0 37 -87 23 -7 57
-78 12 -42 49 95 -31
5 -4 10
87 97 -96 -82
-66 -51 -35 6 73 25 25 81 -74
65 -88 -25 -22 -1 -41 -50 -80 -38 -92
-12 -15 -75 -19 20 22 -42 -78 -37 -93
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
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

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
3
91 14 -19 83 5 61 -88 91 -60
-5 18 30 32 10 86 -76 81 16
-57 45 -14 42 -40 -42
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
False
False
False
```
