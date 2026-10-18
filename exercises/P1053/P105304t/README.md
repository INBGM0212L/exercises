# `P105304t` - Páros számjegyek inkrementálása (végjelig olvasás)

## A függvény
Írj egy `increment_even_digits` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring páros számjegyeinek inkrementálásával kapunk!

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
 | `"0123456789"` | `"1133557799"` |
 | `"a·b·c·d·e·f·g·h"` | `"a·b·c·d·e·f·g·h"` |
 | `"aA······bB"` | `"aA······bB"` |
 | `"A··a·····b···B"` | `"A··a·····b···B"` |
 | `"aB1cD2eF3gH4"` | `"aB1cD3eF3gH5"` |

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
1133557799
a b c d e f g h
aA      bB
A  a     b   B
aB1cD3eF3gH5
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
 00n
4862oak02o6Otpbs8168k
r49caPaP2f80
p82JG8lwYyVg0L P92Grdi 46xMl
ZW7i22XNi86IkMh0Av24m6zs4
U4h6ar
0
0 rQf668YdVM6wE2kQ4
END
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
 11n
5973oak13o7Otpbs9179k
r59caPaP3f91
p93JG9lwYyVg1L P93Grdi 57xMl
ZW7i33XNi97IkMh1Av35m7zs5
U5h7ar
1
1 rQf779YdVM7wE3kQ5
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
Cp40K4e
LvbZ1jn88Lj4T440wfVFcR6xW
vC02bZ3To2
u2 6kA616K403CZo
248Z30e
3BR7m9C200HB4ZyG8B24l4v7
RK4248pS 2ZT88UM2q2Vf
x54gVIbD84Ef
InXsqR0Z30Yh
24AYfA 41p2KHC4N4c0xm28eM1P46
END
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
Cp51K5e
LvbZ1jn99Lj5T551wfVFcR7xW
vC13bZ3To3
u3 7kA717K513CZo
359Z31e
3BR7m9C311HB5ZyG9B35l5v7
RK5359pS 3ZT99UM3q3Vf
x55gVIbD95Ef
InXsqR1Z31Yh
35AYfA 51p3KHC5N5c1xm39eM1P57
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
o4go16ICbMcF0AqsrHP3a4nLy
v0bMO0h4
0fOga07SRN200428wQBDRcJ
8LyGx4
Z2m2Djj64ms0E64KSTBU
vF06UO8 MWH286IsIE
END
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
o5go17ICbMcF1AqsrHP3a5nLy
v1bMO1h5
1fOga17SRN311539wQBDRcJ
9LyGx5
Z3m3Djj75ms1E75KSTBU
vF17UO9 MWH397IsIE
```
