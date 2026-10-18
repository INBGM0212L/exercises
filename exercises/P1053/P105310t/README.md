# `P105310t` - Páratlan számjegyek dekrementálása (végjelig olvasás)

## A függvény
Írj egy `decrement_odd_digits` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring páratlan számjegyeinek dekrementálásával kapunk!

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
 | `"0123456789"` | `"0022446688"` |
 | `"a·b·c·d·e·f·g·h"` | `"a·b·c·d·e·f·g·h"` |
 | `"aA······bB"` | `"aA······bB"` |
 | `"A··a·····b···B"` | `"A··a·····b···B"` |
 | `"aB1cD2eF3gH4"` | `"aB0cD2eF2gH4"` |

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
0022446688
a b c d e f g h
aA      bB
A  a     b   B
aB0cD2eF2gH4
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
f65kf
7wr 5lRa1an9951XAZ3p1EPk
CvYS1s3hw395mXI3V9e3y
mphg3
END
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
f64kf
6wr 4lRa0an8840XAZ2p0EPk
CvYS0s2hw284mXI2V8e2y
mphg2
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
n333519Nf5W3PPG971hA
dTplS313
1BzuqXZuD83R07V03Ri1Vx2FlnxY7U
V0VF99
XNR2KHRDy75o97Vv1597
i3zdb943D WsC185o6
7tBg3G6D76nKpcK973z73xk
END
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
n222408Nf4W2PPG860hA
dTplS202
0BzuqXZuD82R06V02Ri0Vx2FlnxY6U
V0VF88
XNR2KHRDy64o86Vv0486
i2zdb842D WsC084o6
6tBg2G6D66nKpcK862z62xk
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
7190v5aYr 9
g3uR6x15n1V4TK
97FJ U17150gd1ILI15n9U51P
5eb70Vg1QdQR9185L77EcPOQ3U
kT151YHl11ls3K325cS
sY17R7wAyFCD1
53i7Ql7EW9R9t8xmUkZx39IaC9M99
END
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
6080v4aYr 8
g2uR6x04n0V4TK
86FJ U06040gd0ILI04n8U40P
4eb60Vg0QdQR8084L66EcPOQ2U
kT040YHl00ls2K224cS
sY06R6wAyFCD0
42i6Ql6EW8R8t8xmUkZx28IaC8M88
```
