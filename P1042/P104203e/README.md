# `P104203e` - Szigorúan monoton növekvő lista (állományvégjelig olvasás)

## A függvény
Írj egy `is_strictly_monotone_increasing` nevű függvényt, mely visszaadja azt, hogy a paraméterként megkapott lista elemei szigorúan monoton nökvekvő sorozatot alkotnak-e!


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
 | `[1, 1, 1, 1]` | `False` |
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
True
False
False
False
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
67 -35 -82 64 -57 6 -50
45 -23 82 0
4 -13 -2 6 53 -84
-10 53 40 -34 -65 -4 18 0 63 -49
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
36 -41 -84 25 32 69
33 -1 32 87
38 -98
19 44 23 -85 -39 -60 -29 -7
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
False
False
False
False
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
23 89 89 -61 39 8 3 9 8
89 -74 -37 56
39 -78 69 -37 -42 62
83 -74 -72 64
-64
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
False
False
False
False
True
```
