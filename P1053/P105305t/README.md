# `P105305t` - Páratlan számjegyek inkrementálása (végjelig olvasás)

## A függvény
Írj egy `increment_odd_digits` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring páratlan számjegyeinek inkrementálásával kapunk!

### Magyarázat
Egy számjegy inkrementálása alatt azt a műveletet értjük, mely során a számjegyet az érték szerint őt követő számjeggyel helyettesítjük. Például a `0` karaktert az `1` karakterre, míg az `1` karaktert a `2` karakterre cseréljük. A `9` karaktert az `0` karakterrel kell helyettesíteni.

### Paraméterlista
1. `original` - az eredeti sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az átalakított sztring

### Példák
 | `original` | Visszaadott érték |
 | :--- | :-- |
 | `"abcdefghijklmnopqrstuvwxyz"` | `"abcdefghijklmnopqrstuvwxyz"` |
 | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` |
 | `"0123456789"` | `"0224466880"` |
 | `"a·b·c·d·e·f·g·h"` | `"a·b·c·d·e·f·g·h"` |
 | `"aA······bB"` | `"aA······bB"` |
 | `"A··a·····b···B"` | `"A··a·····b···B"` |
 | `"aB1cD2eF3gH4"` | `"aB2cD2eF4gH4"` |

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
0224466880
a b c d e f g h
aA      bB
A  a     b   B
aB2cD2eF4gH4
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
WCJtBZ2f3Mv97gBMA
m9M757X19
9Vc5UZh
w478l95
x9r3D7aCl
5 DZ5
END
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
WCJtBZ2f4Mv08gBMA
m0M868X20
0Vc6UZh
w488l06
x0r4D8aCl
6 DZ6
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
yiga7je9E9ed5ilq
11U5358N1y0131
9txQoyk52o1jw
9I9XfJ7Ec5JSA5k9HauL9
17 e2xHoq5P1Cs1C7g
END
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
yiga8je0E0ed6ilq
22U6468N2y0242
0txQoyk62o2jw
0I0XfJ8Ec6JSA6k0HauL0
28 e2xHoq6P2Cs2C8g
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
zahI1zb56Th77lE5uspEh56a23C
e5PLy9X7543Xm3
9w
hF8 9t9IAevIgygz33mI9
END
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
zahI2zb66Th88lE6uspEh66a24C
e6PLy0X8644Xm4
0w
hF8 0t0IAevIgygz44mI0
```
