# `P105206n` - Mássalhangzók duplikálása (`n` teszteset)

## A függvény
Írj egy `double_consonants` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring mássalhangzóinak megkettőzésével kapunk!


### Paraméterlista
1. `original` - az eredeti sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az átalakított sztring

### Példák
 | `original` | Visszaadott érték |
 | :--- | :-- |
 | `"abcdefghijklmnopqrstuvwxyz"` | `"abbccddeffgghhijjkkllmmnnoppqqrrssttuvvwwxxyyzz"` |
 | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `"ABBCCDDEFFGGHHIJJKKLLMMNNOPPQQRRSSTTUVVWWXXYYZZ"` |
 | `"0123456789"` | `"0123456789"` |
 | `"a·b·c·d·e·f·g·h"` | `"a·bb·cc·dd·e·ff·gg·hh"` |
 | `"aA······bB"` | `"aA······bbBB"` |
 | `"A··a·····b···B"` | `"A··a·····bb···BB"` |
 | `"aB1cD2eF3gH4"` | `"aBB1ccDD2eFF3ggHH4"` |

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
abbccddeffgghhijjkkllmmnnoppqqrrssttuvvwwxxyyzz
ABBCCDDEFFGGHHIJJKKLLMMNNOPPQQRRSSTTUVVWWXXYYZZ
0123456789
a bb cc dd e ff gg hh
aA      bbBB
A  a     bb   BB
aBB1ccDD2eFF3ggHH4
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
3
n00XZbmjI1vlvqgadrxj
xMgydGjbgBWk
r1Z6m
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
nn00XXZZbbmmjjI1vvllvvqqggaddrrxxjj
xxMMggyyddGGjjbbggBBWWkk
rr1ZZ6mm
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
10
nmrL
mG
vGqxhddxAJjPqftotQnsn3hbgmxP
j1uNCHd
fRylGrylTLvylSg7A
bh0w7UOgfptADqgEOwwvVQm
jmuJOwrhrpwgfhwUqI qOk
aqnKjUqbjwyg
nzyHgcf
ebtkDc9T2zFp
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
nnmmrrLL
mmGG
vvGGqqxxhhddddxxAJJjjPPqqffttottQQnnssnn3hhbbggmmxxPP
jj1uNNCCHHdd
ffRRyyllGGrryyllTTLLvvyyllSSgg7A
bbhh0ww7UOggffppttADDqqggEOwwwwvvVVQQmm
jjmmuJJOwwrrhhrrppwwggffhhwwUqqI qqOkk
aqqnnKKjjUqqbbjjwwyygg
nnzzyyHHggccff
ebbttkkDDcc9TT2zzFFpp
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
4
3txdqcv3
scjcqhd
vhh0fjztp0h6K
jn
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
3ttxxddqqccvv3
ssccjjccqqhhdd
vvhhhh0ffjjzzttpp0hh6KK
jjnn
```
