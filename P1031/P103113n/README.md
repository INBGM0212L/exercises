# `P103113n` - Kör kerekített kerülete (`n` teszteset)

## A függvény
Írj egy `circle_circumference_rounded` nevű függvényt, mely visszaadja a paraméterként megkapott `r` sugarú kör kerületét `d` tizedesjegyre kerekítve!


### Paraméterlista
1. `r` - a kör sugara (egész érték a(z) `[1,100]` intervallumból)
2. `d` - a kerekítés pontossága (egész érték a(z) `[0,7]` intervallumból)

### Visszaadott érték
* a kör kerekített kerülete

### Példák
 | `r` | `d` | Visszaadott érték |
 | :--- | :--- | :-- |
 | `5` | `2` | `31.42` |
 | `25` | `4` | `157.0796` |
 | `35` | `1` | `219.9` |
 | `10` | `7` | `62.8318531` |
 | `92` | `6` | `578.053048` |
 | `2` | `3` | `12.566` |
 | `31` | `0` | `195.0` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek száma az első sorban szereplő egész érték.
* Minden tesztesetet egy külön sor ír le, melyben a függvény argumentumai (`r` és `d`) szerepelnek egy-egy szóközzel elválasztva egymástól, ebben a sorrendben.

## Megjegyzés a *C* nyelvű megoldásokhoz
A példákban látható értékeket egy Python nyelvű megoldás  Előfordulhat, hogy a két nyelv kerekítési hibája nem pontosan ugyanaz valós értékeknél.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |
| `test-03` | [`test-03.in`](test-03.in) | [`test-03.out`](test-03.out) |

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
7
5 2
25 4
35 1
10 7
92 6
2 3
31 0
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
31.42
157.0796
219.9
62.8318531
578.053048
12.566
195.0
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
7
99 3
24 4
92 7
87 1
29 7
63 7
77 5
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
622.035
150.7964
578.0530483
546.6
182.2123739
395.8406744
483.80527
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
7
32 4
17 6
15 1
78 1
49 3
74 1
25 5
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
201.0619
106.81415
94.2
490.1
307.876
465.0
157.07963
```
