# `P103207t` - Ikerprímek (végjelig olvasás)

## A függvény
Írj egy `are_twin_primes` nevű függvényt, mely visszaadja azt, hogy a paraméterként megkapott értékek ikerprímet alkotnak-e vagy sem!


### Paraméterlista
1. `n` - az első tesztelendő érték (egész érték a(z) `[1,10]` intervallumból)
2. `m` - a második tesztelendő érték (egész érték a(z) `[1,10]` intervallumból)

### Visszaadott érték
* `True`, ha `n` és `m` ikerprímek, egyébként `False`

### Példák
 | `n` | `m` | Visszaadott érték |
 | :--- | :--- | :-- |
 | `1` | `2` | `False` |
 | `2` | `3` | `False` |
 | `3` | `5` | `True` |
 | `5` | `3` | `True` |
 | `7` | `9` | `False` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek végét a következő sor jelzi (melyet már nem kell feldolgozni): `"0"`
* Minden tesztesetet egy külön sor ír le, melyben a függvény argumentumai (`n` és `m`) szerepelnek egy-egy szóközzel elválasztva egymástól, ebben a sorrendben.

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
1 2
2 3
3 5
5 3
7 9
0
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
False
False
True
True
False
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
9 9
6 3
10 9
4 7
10 3
3 5
6 10
2 3
0
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
False
False
False
False
False
True
False
False
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
4 9
3 6
10 2
0
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
False
False
False
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
6 3
7 3
8 7
4 1
2 6
2 10
6 6
6 5
0
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
False
False
False
False
False
False
False
False
```
