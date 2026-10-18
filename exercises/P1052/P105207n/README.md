# `P105207n` - Páros számjegyek duplikálása (`n` teszteset)

## A függvény
Írj egy `double_even_digits` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring páros számjegyeinek megkettőzésével kapunk!


### Paraméterlista
1. `original` - az eredeti sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az átalakított sztring

### Példák
 | `original` | Visszaadott érték |
 | :--- | :-- |
 | `"abcdefghijklmnopqrstuvwxyz"` | `"abcdefghijklmnopqrstuvwxyz"` |
 | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` |
 | `"0123456789"` | `"001223445667889"` |
 | `"a·b·c·d·e·f·g·h"` | `"a·b·c·d·e·f·g·h"` |
 | `"aA······bB"` | `"aA······bB"` |
 | `"A··a·····b···B"` | `"A··a·····b···B"` |
 | `"aB1cD2eF3gH4"` | `"aB1cD22eF3gH44"` |

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
001223445667889
a b c d e f g h
aA      bB
A  a     b   B
aB1cD22eF3gH44
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
3
0fi8Bf8kFnh990A6 M0Io68f8eW
BmT202zd2rSO58
726etZi8Q
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
00fi88Bf88kFnh9900A66 M00Io6688f88eW
BmT220022zd22rSO588
72266etZi88Q
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
4
700qt2O8nvIU6FC76v
48TNU66YX0VF0006fTDJSW8x4eg
P1A029FsfEd
zf
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
70000qt22O88nvIU66FC766v
4488TNU6666YX00VF00000066fTDJSW88x44eg
P1A00229FsfEd
zf
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
9
1LTv2KYO3
8d6H6SN62
5DXk4I7s1p3At06Idl40uX
yhZ461tk4R9mQg
g0244xXmgy42XUn2
098Ix08e42z0F0 PI0Dz030r3
j0BmBu686Ky2HPxS18T829dNE8MyKp
c4ZqrY2mRo93820Iwv
Ie
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
1LTv22KYO3
88d66H66SN6622
5DXk44I7s1p3At0066Idl4400uX
yhZ44661tk44R9mQg
g00224444xXmgy4422XUn22
00988Ix0088e4422z00F00 PI00Dz00300r3
j00BmBu668866Ky22HPxS188T88229dNE88MyKp
c44ZqrY22mRo93882200Iwv
Ie
```
