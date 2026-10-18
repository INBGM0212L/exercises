# `P105208n` - Páratlan számjegyek duplikálása (`n` teszteset)

## A függvény
Írj egy `double_odd_digits` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring páratlan számjegyeinek megkettőzésével kapunk!


### Paraméterlista
1. `original` - az eredeti sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az átalakított sztring

### Példák
 | `original` | Visszaadott érték |
 | :--- | :-- |
 | `"abcdefghijklmnopqrstuvwxyz"` | `"abcdefghijklmnopqrstuvwxyz"` |
 | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` |
 | `"0123456789"` | `"011233455677899"` |
 | `"a·b·c·d·e·f·g·h"` | `"a·b·c·d·e·f·g·h"` |
 | `"aA······bB"` | `"aA······bB"` |
 | `"A··a·····b···B"` | `"A··a·····b···B"` |
 | `"aB1cD2eF3gH4"` | `"aB11cD2eF33gH4"` |

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
7
abcdefghijklmnopqrstuvwxyz
ABCDEFGHIJKLMNOPQRSTUVWXYZ
0123456789
a b c d e f g h
aA      bB
A  a     b   B
aB1cD2eF3gH4
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
abcdefghijklmnopqrstuvwxyz
ABCDEFGHIJKLMNOPQRSTUVWXYZ
011233455677899
a b c d e f g h
aA      bB
A  a     b   B
aB11cD2eF33gH4
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
8
cbK7bsw217p1UzwjFg
 M97w397
75n5VF37aQ
Ism379G1vZu3Z9
2y59j9lBA35j1S57aA3595
w6
K53d
3d7NOqoi33prJobP1HVgs1aX1l1
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
cbK77bsw21177p11UzwjFg
 M9977w339977
7755n55VF3377aQ
Ism337799G11vZu33Z99
2y5599j99lBA3355j11S5577aA33559955
w6
K5533d
33d77NOqoi3333prJobP11HVgs11aX11l11
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
9
5o
dPRrR3C991a3v1
GHpplB
9N1Y9U4yUN7w3
SeW
323330E9xv3E8
A5e1N55C90K5huLq04LE95pqwF7XF
g13E7EY6K37yIEM 9p53w
4
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
55o
dPRrR33C999911a33v11
GHpplB
99N11Y99U4yUN77w33
SeW
3323333330E99xv33E8
A55e11N5555C990K55huLq04LE9955pqwF77XF
g1133E77EY6K3377yIEM 99p5533w
4
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
10
LG5V7Z4hOv9kEQR1Nc07XyS
3r3lSL5i3c
HC5
c51Pkx114CJthz
52
q9O79IPamisR
9zg53wbvpW19Wn55
1399T318K9iAu15 aCS9573O0iW953
HPXJKkrgeZD
Njf
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
LG55V77Z4hOv99kEQR11Nc077XyS
33r33lSL55i33c
HC55
c5511Pkx11114CJthz
552
q99O7799IPamisR
99zg5533wbvpW1199Wn5555
11339999T33118K99iAu1155 aCS99557733O0iW995533
HPXJKkrgeZD
Njf
```
