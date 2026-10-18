# `P103105t` - Négyzet kerülete (végjelig olvasás)

## A függvény
Írj egy `square_circumference` nevű függvényt, mely visszaadja a paraméterként megkapott oldalhosszúságú négyzet kerületét!


### Paraméterlista
1. `n` - a négyzet oldalhossza (egész érték a(z) `[1,100]` intervallumból)

### Visszaadott érték
* a négyzet kerülete

### Példák
 | `n` | Visszaadott érték |
 | :--- | :-- |
 | `8` | `32` |
 | `48` | `192` |
 | `26` | `104` |
 | `92` | `368` |
 | `4` | `16` |
 | `46` | `184` |
 | `7` | `28` |
 | `25` | `100` |
 | `65` | `260` |
 | `80` | `320` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* Minden tesztesetet pontosan egy sor ír le, melyben a függvény argumentuma (`n`) szerepel.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |
| `test-03` | [`test-03.in`](test-03.in) | [`test-03.out`](test-03.out) |

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
8
48
26
92
4
46
7
25
65
80
0
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
32
192
104
368
16
184
28
100
260
320
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
10
70
18
0
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
40
280
72
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
98
53
3
94
73
0
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
392
212
12
376
292
```
