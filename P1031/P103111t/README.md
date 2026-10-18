# `P103111t` - Kör kerülete (végjelig olvasás)

## A függvény
Írj egy `circle_circumference` nevű függvényt, mely visszaadja a paraméterként megkapott sugarú kör kerületét!


### Paraméterlista
1. `r` - a kör sugara (egész érték a(z) `[1,100]` intervallumból)

### Visszaadott érték
* a kör kerülete

### Példák
 | `r` | Visszaadott érték |
 | :--- | :-- |
 | `14` | `87.96459430051421` |
 | `67` | `420.97341558103227` |
 | `44` | `276.46015351590177` |
 | `6` | `37.69911184307752` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* Minden tesztesetet pontosan egy sor ír le, melyben a függvény argumentuma (`r`) szerepel.

## Megjegyzés a *C* nyelvű megoldásokhoz
A példákban látható értékeket egy *Python* nyelvű megoldás állította elő. Lehetséges hogy a két nyelv kerekítési hibája nem pontosan ugyanaz valós értékeknél.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |
| `test-03` | [`test-03.in`](test-03.in) | [`test-03.out`](test-03.out) |

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
14
67
44
6
0
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
87.96459430051421
420.97341558103227
276.46015351590177
37.69911184307752
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
88
58
56
25
47
0
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
552.9203070318035
364.424747816416
351.85837720205683
157.07963267948966
295.3097094374406
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
54
18
69
32
66
75
22
0
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
339.29200658769764
113.09733552923255
433.53978619539146
201.06192982974676
414.6902302738527
471.23889803846896
138.23007675795088
```
