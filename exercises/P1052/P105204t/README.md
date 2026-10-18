# `P105204t` - Számjegyek duplikálása (végjelig olvasás)

## A függvény
Írj egy `double_digits` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring számjegyeinek megkettőzésével kapunk!


### Paraméterlista
1. `original` - az eredeti sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az átalakított sztring

### Példák
 | `original` | Visszaadott érték |
 | :--- | :-- |
 | `"abcdefghijklmnopqrstuvwxyz"` | `"abcdefghijklmnopqrstuvwxyz"` |
 | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` |
 | `"0123456789"` | `"00112233445566778899"` |
 | `"a·b·c·d·e·f·g·h"` | `"a·b·c·d·e·f·g·h"` |
 | `"aA······bB"` | `"aA······bB"` |
 | `"A··a·····b···B"` | `"A··a·····b···B"` |
 | `"aB1cD2eF3gH4"` | `"aB11cD22eF33gH44"` |

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
00112233445566778899
a b c d e f g h
aA      bB
A  a     b   B
aB11cD22eF33gH44
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
7
568 61k8HR6518Pmc2j1X
K1EG6tTL99XD40Uq135
J964JP
B72580JT5
END
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
77
556688 6611k88HR66551188Pmc22j11X
K11EG66tTL9999XD4400Uq113355
J996644JP
B7722558800JT55
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
SHv73id51Kmpe
08753f8
P6bOj378B598aOm380013 8
9L7DC463255wNL3JFk9ah1
2126HiX46p1cV
END
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
SHv7733id5511Kmpe
0088775533f88
P66bOj337788B559988aOm338800001133 88
99L77DC446633225555wNL33JFk99ah11
22112266HiX4466p11cV
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
Y59t4tm01038 swY1I84H695b6
d3e3TE62wxV997A0U36V686Jfi9n52
c23veu5B4F236K15zMeWL104x8M
xZ81W3n04b85YXbD66Cs9z88m3
END
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
Y5599t44tm0011003388 swY11I8844H669955b66
d33e33TE6622wxV999977A00U3366V668866Jfi99n5522
c2233veu55B44F223366K1155zMeWL110044x88M
xZ8811W33n0044b8855YXbD6666Cs99z8888m33
```
