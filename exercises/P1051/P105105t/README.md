# `P105105t` - Magánhangzók eltávolítása (végjelig olvasás)

## A függvény
Írj egy `delete_vowels` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring magánhangzóinak törlésével kapunk!


### Paraméterlista
1. `original` - az eredeti sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az átalakított sztring

### Példák
 | `original` | Visszaadott érték |
 | :--- | :-- |
 | `"abcdefghijklmnopqrstuvwxyz"` | `"bcdfghjklmnpqrstvwxyz"` |
 | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `"BCDFGHJKLMNPQRSTVWXYZ"` |
 | `"0123456789"` | `"0123456789"` |
 | `"a·b·c·d·e·f·g·h"` | `"·b·c·d··f·g·h"` |
 | `"aA······bB"` | `"······bB"` |
 | `"A··a·····b···B"` | `"·······b···B"` |
 | `"aB1cD2eF3gH4"` | `"B1cD2F3gH4"` |

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
bcdfghjklmnpqrstvwxyz
BCDFGHJKLMNPQRSTVWXYZ
0123456789
 b c d  f g h
      bB
       b   B
B1cD2F3gH4
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
aoZ
iuWauoZwlAaOeogeWaYudi
quDueuEuieaauiAUiHoX
END
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
Z
WZwlgWYd
qDHX
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
5aNaVdoe4epVEyaoeWiijp1ja7a1ou
u4aT2u3e1L8iuhiT
Ew4vu
BiiXqlao
fuaa8cRe9ofbeioSeehbu3ze4oeue8
eitEPuui
e ov0eqeuHsmiPRuNj Cotef
END
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
5NVd4pVyWjp1j71
4T231L8hT
w4v
BXql
f8cR9fbShb3z48
tP
 v0qHsmPRNj Ctf
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
IOZ
uqJzhG2lGoKamcrRDaW
ukl
END
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
Z
qJzhG2lGKmcrRDW
kl
```
