# `P105202t` - Kisbetűk duplikálása (végjelig olvasás)

## A függvény
Írj egy `double_lowers` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring kisbetűinek megkettőzésével kapunk!


### Paraméterlista
1. `original` - az eredeti sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az átalakított sztring

### Példák
 | `original` | Visszaadott érték |
 | :--- | :-- |
 | `"abcdefghijklmnopqrstuvwxyz"` | `"aabbccddeeffgghhiijjkkllmmnnooppqqrrssttuuvvwwxxyyzz"` |
 | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` |
 | `"0123456789"` | `"0123456789"` |
 | `"a·b·c·d·e·f·g·h"` | `"aa·bb·cc·dd·ee·ff·gg·hh"` |
 | `"aA······bB"` | `"aaA······bbB"` |
 | `"A··a·····b···B"` | `"A··aa·····bb···B"` |
 | `"aB1cD2eF3gH4"` | `"aaB1ccD2eeF3ggH4"` |

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
aabbccddeeffgghhiijjkkllmmnnooppqqrrssttuuvvwwxxyyzz
ABCDEFGHIJKLMNOPQRSTUVWXYZ
0123456789
aa bb cc dd ee ff gg hh
aaA      bbB
A  aa     bb   B
aaB1ccD2eeF3ggH4
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
r3Kybh2lSzPh
baRFzdkFfihIJ9pwiA9 ehwg4wOT
bav5Kwmv0utanJjk7
END
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
rr3Kyybbhh2llSzzPhh
bbaaRFzzddkkFffiihhIJ9ppwwiiA9 eehhwwgg4wwOT
bbaavv5Kwwmmvv0uuttaannJjjkk7
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
lR3nIIcj
GaqdlXxtLHSj
9vAExLWQ Fjg
uNdleu
END
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
llR3nnIIccjj
GaaqqddllXxxttLHSjj
9vvAExxLWQ Fjjgg
uuNddlleeuu
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
f
nyBIL
yhc9BrAt4qniXkA
lmuh
mWmovzsd BhfO I6vABf9Wjs5Am48
END
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
ff
nnyyBIL
yyhhcc9BrrAtt4qqnniiXkkA
llmmuuhh
mmWmmoovvzzssdd BhhffO I6vvABff9Wjjss5Amm48
```
