# `P103107n` - Téglalap kerülete (`n` teszteset)

## A függvény
Írj egy `rectangle_circumference` nevű függvényt, mely visszaadja a paraméterként megkapott oldalhosszúságú téglalap kerületét!


### Paraméterlista
1. `a` - az `a` oldal hossza (egész érték a(z) `[1,100]` intervallumból)
2. `b` - a `b` oldal hossza (egész érték a(z) `[1,100]` intervallumból)

### Visszaadott érték
* a téglalap kerülete

### Példák
 | `a` | `b` | Visszaadott érték |
 | :--- | :--- | :-- |
 | `28` | `10` | `76` |
 | `45` | `5` | `100` |
 | `78` | `30` | `216` |
 | `22` | `29` | `102` |
 | `15` | `62` | `154` |
 | `26` | `8` | `68` |
 | `88` | `45` | `266` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek száma az első sorban szereplő egész érték.
* Minden tesztesetet egy külön sor ír le, melyben a függvény argumentumai (`a` és `b`) szerepelnek egy-egy szóközzel elválasztva egymástól, ebben a sorrendben.

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
28 10
45 5
78 30
22 29
15 62
26 8
88 45
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
76
100
216
102
154
68
266
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
3
71 86
49 54
89 100
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
314
206
378
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
4
42 75
31 95
89 24
11 60
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
234
252
226
142
```
