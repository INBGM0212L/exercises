# `P104207e` - Váltakozó előjelű lista (állományvégjelig olvasás)

## A függvény
Írj egy `is_twisting` nevű függvényt, mely visszaadja azt, hogy a paraméterként megkapott lista elemeire felváltva teljesül-e az, hogy negatívak-e vagy sem (azaz egy negatív elemet egy nemnegatív elem követ, míg egy nemnegatív elemet egy negatív)!


### Paraméterlista
1. `numbers` - az ellenőrizendő lista (egy legalább `1`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `-99`, legfeljebb `99`)

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
 | `[1, 2, 3, 5, 8, 13]` | `False` |
 | `[-1, -2, -3, -5, -8, -13]` | `False` |
 | `[10, 20, 30, 50, 80, 130]` | `False` |
 | `[1, -2, 3, -4, 5, -6]` | `True` |
 | `[1, 2, 1, 2]` | `False` |
 | `[1, -3]` | `True` |


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
False
False
True
True
False
False
False
True
False
True
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
-54
52 -4 -16 -88 -54 -35 -22 25
-4 -34
38 48 59 63 -43 -35 61 99 -55 -74
4 -87 63 46 -96 11 4 63 -81
-76 -41 62 6 92 -39
-2 42 -63 -93 -30 42
-64 69
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
True
False
False
False
False
False
False
True
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
-41 -68 64 -59 95 -80 37 -1 -50 -87
-57 -82 83 -67 -34 45
41 -61 23
-73 -68 -97 95 -45
-61 35 -52 -90
-23
-29 -58 44 -80 -43 -14 18 -60
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
False
False
True
False
False
True
False
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
13
-60 28 -35 99 -84 -17 -15 2 38
-86 -12 -41 -75 -25 61 67 94
-64
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
True
False
False
True
```
