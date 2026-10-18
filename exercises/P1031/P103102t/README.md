# `P103102t` - Előjel fordítás (végjelig olvasás)

## A függvény
Írj egy `change_signature` nevű függvényt, mely visszaadja a paraméterként megkapott érték ellentettjét!


### Paraméterlista
1. `n` - az `n` értéke (egész érték a(z) `[-100,100]` intervallumból)

### Visszaadott érték
* az `n` ellentettje

### Példák
 | `n` | Visszaadott érték |
 | :--- | :-- |
 | `80` | `-80` |
 | `-81` | `81` |
 | `-36` | `36` |
 | `44` | `-44` |


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
80
-81
-36
44
999
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
-80
81
36
-44
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
-69
-90
-40
999
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
69
90
40
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
-19
-87
-55
999
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
19
87
55
```
