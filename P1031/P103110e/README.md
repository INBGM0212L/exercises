# `P103110e` - Kör területe (állományvégjelig olvasás)

## A függvény
Írj egy `circle_area` nevű függvényt, mely visszaadja a paraméterként megkapott sugarú kör területét!


### Paraméterlista
1. `r` - a kör sugara (egész érték a(z) `[1,100]` intervallumból)

### Visszaadott érték
* a kör területe

### Példák
 | `r` | Visszaadott érték |
 | :--- | :-- |
 | `12` | `452.3893421169302` |
 | `23` | `1661.9025137490005` |
 | `47` | `6939.778171779853` |
 | `18` | `1017.8760197630929` |
 | `46` | `6647.610054996002` |
 | `24` | `1809.5573684677208` |


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
12
23
47
18
46
24
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
452.3893421169302
1661.9025137490005
6939.778171779853
1017.8760197630929
6647.610054996002
1809.5573684677208
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
99
68
47
39
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
30790.74959783356
14526.724430199203
6939.778171779853
4778.362426110075
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
61
99
43
26
16
74
18
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
11689.86626400762
30790.74959783356
5808.804816487527
2123.7166338267
804.247719318987
17203.36137105771
1017.8760197630929
```
