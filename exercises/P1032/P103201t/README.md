# `P103201t` - Legnagyobb közös osztó (végjelig olvasás)

## A függvény
Írj egy `gcd` nevű függvényt, mely visszaadja a paraméterként megkapott két szám (`a` és `b`) legnagyobb közös osztóját!


### Paraméterlista
1. `a` - az `a` értéke (egész érték a(z) `[1,100]` intervallumból)
2. `b` - a `b` értéke (egész érték a(z) `[1,100]` intervallumból)

### Visszaadott érték
* a legnagyobb közös osztó

### Példák
 | `a` | `b` | Visszaadott érték |
 | :--- | :--- | :-- |
 | `79` | `21` | `1` |
 | `49` | `41` | `1` |
 | `64` | `22` | `2` |
 | `32` | `31` | `1` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek végét a következő sor jelzi (melyet már nem kell feldolgozni): `"0"`
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
79 21
49 41
64 22
32 31
0
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
1
1
2
1
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
98 45
46 89
31 1
4 67
86 70
28 72
50 2
39 24
87 46
30 15
0
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
1
1
1
1
2
4
2
3
1
15
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
90 97
70 81
27 78
71 92
88 50
0
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
1
1
3
1
2
```
