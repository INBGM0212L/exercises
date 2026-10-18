# `P103101t` - Echo (végjelig olvasás)

## A függvény
Írj egy `echo` nevű függvényt, mely visszaadja a paraméterként megkapott értéket mindenféle módosítás nélkül!


### Paraméterlista
1. `n` - az `n` értéke (egész érték a(z) `[-100,100]` intervallumból)

### Visszaadott érték
* az `n` értéke

### Példák
 | `n` | Visszaadott érték |
 | :--- | :-- |
 | `-33` | `-33` |
 | `23` | `23` |
 | `39` | `39` |
 | `61` | `61` |
 | `48` | `48` |
 | `16` | `16` |


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
-33
23
39
61
48
16
999
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
-33
23
39
61
48
16
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
-68
-20
-21
-43
999
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
-68
-20
-21
-43
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
75
70
18
-49
73
999
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
75
70
18
-49
73
```
