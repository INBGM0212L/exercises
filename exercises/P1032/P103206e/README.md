# `P103206e` - Prímteszt (állományvégjelig olvasás)

## A függvény
Írj egy `is_prime` nevű függvényt, mely visszaadja azt, hogy a paraméterként megkapott érték prímszám-e vagy sem!


### Paraméterlista
1. `n` - a tesztelendő érték (egész érték a(z) `[1,1000]` intervallumból)

### Visszaadott érték
* `True`, ha `n` prím, egyébként `False`

### Példák
 | `n` | Visszaadott érték |
 | :--- | :-- |
 | `1` | `False` |
 | `2` | `True` |
 | `3` | `True` |
 | `4` | `False` |
 | `5` | `True` |
 | `49` | `False` |
 | `101` | `True` |
 | `113` | `True` |
 | `999` | `False` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* Minden tesztesetet pontosan egy sor ír le, melyben a függvény argumentuma (`n`) szerepel.

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
1
2
3
4
5
49
101
113
999
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
False
True
True
False
True
False
True
True
False
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
519
932
312
230
146
752
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
False
False
False
False
False
False
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
703
682
285
931
682
310
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
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
43
832
146
822
238
653
808
632
242
854
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
True
False
False
False
False
True
False
False
False
False
```
