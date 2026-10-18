# `P105309t` - Páros számjegyek dekrementálása (végjelig olvasás)

## A függvény
Írj egy `decrement_even_digits` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring páros számjegyeinek dekrementálásával kapunk!

### Magyarázat
Egy számjegy dekrementálása alatt azt a műveletet értjük, mely során a számjegyet az érték szerint őt megelőző számjeggyel helyettesítjük. Például a `2` karaktert az `1` karakterre, míg az `1` karaktert a `0` karakterre cseréljük. A `0` karaktert a `9` karakterrel kell helyettesíteni.

### Paraméterlista
1. `original` - az eredeti sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az átalakított sztring

### Példák
 | `original` | Visszaadott érték |
 | :--- | :-- |
 | `"abcdefghijklmnopqrstuvwxyz"` | `"abcdefghijklmnopqrstuvwxyz"` |
 | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` |
 | `"0123456789"` | `"9113355779"` |
 | `"a·b·c·d·e·f·g·h"` | `"a·b·c·d·e·f·g·h"` |
 | `"aA······bB"` | `"aA······bB"` |
 | `"A··a·····b···B"` | `"A··a·····b···B"` |
 | `"aB1cD2eF3gH4"` | `"aB1cD1eF3gH3"` |

A paraméterekhez tartozó literálokban minden `' '` (szóköz) karakter a `'·'` (pont) karakterrel kerül helyettesítésre.


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* Minden tesztesetet pontosan egy sor ír le, melyben a függvény argumentuma (`original`) szerepel.

## Megjegyzés a *C* nyelvű megoldásokhoz
* A függvény egy dinamikusan foglalt tömb kezdőcímét adja vissza.
* A főprogram felszabadítja a tömb mögött álló memóriaterületet.

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
abcdefghijklmnopqrstuvwxyz
ABCDEFGHIJKLMNOPQRSTUVWXYZ
0123456789
a b c d e f g h
aA      bB
A  a     b   B
aB1cD2eF3gH4
END
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
abcdefghijklmnopqrstuvwxyz
ABCDEFGHIJKLMNOPQRSTUVWXYZ
9113355779
a b c d e f g h
aA      bB
A  a     b   B
aB1cD1eF3gH3
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
4h9z41pzIOHa4X
T6Wb466PV8
Wp42B4TFsB1cOt242q0kAx4UG
b9MU
END
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
3h9z31pzIOHa3X
T5Wb355PV7
Wp31B3TFsB1cOt131q9kAx3UG
b9MU
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
Q
fCWApB2L6Q0HdQ098
Qm6OPCk
0OTqR7FrX3c
388bH37M4Fh2
8SFUYj862L4U4Qz7D6j Q8j
END
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
Q
fCWApB1L5Q9HdQ997
Qm5OPCk
9OTqR7FrX3c
377bH37M3Fh1
7SFUYj751L3U3Qz7D5j Q7j
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
OBu6E88y
z46v2AP64IFy20Q046
e4NFk88GM0g8Jf4v8QxZ3diW6Z
278L2U82se0o2yIVIkB8
END
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
OBu5E77y
z35v1AP53IFy19Q935
e3NFk77GM9g7Jf3v7QxZ3diW5Z
177L1U71se9o1yIVIkB7
```
