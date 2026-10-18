# `P105205e` - Magánhangzók duplikálása (állományvégjelig olvasás)

## A függvény
Írj egy `double_vowels` nevű függvényt, mely visszaadja azt a sztringet, melyet a paraméterként megkapott sztring magánhangzóinak megkettőzésével kapunk!


### Paraméterlista
1. `original` - az eredeti sztring (egy legalább `1`, legfeljebb `30` karakter hosszúságú sztring)

### Visszaadott érték
* az átalakított sztring

### Példák
 | `original` | Visszaadott érték |
 | :--- | :-- |
 | `"abcdefghijklmnopqrstuvwxyz"` | `"aabcdeefghiijklmnoopqrstuuvwxyz"` |
 | `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `"AABCDEEFGHIIJKLMNOOPQRSTUUVWXYZ"` |
 | `"0123456789"` | `"0123456789"` |
 | `"a·b·c·d·e·f·g·h"` | `"aa·b·c·d·ee·f·g·h"` |
 | `"aA······bB"` | `"aaAA······bB"` |
 | `"A··a·····b···B"` | `"AA··aa·····b···B"` |
 | `"aB1cD2eF3gH4"` | `"aaB1cD2eeF3gH4"` |

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
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
aabcdeefghiijklmnoopqrstuuvwxyz
AABCDEEFGHIIJKLMNOOPQRSTUUVWXYZ
0123456789
aa b c d ee f g h
aaAA      bB
AA  aa     b   B
aaB1cD2eeF3gH4
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
ieOfFixdVgeiordop8ayYG5e1yueJi
nTauPeueTeuenBoDTIyivoomzeuA
eDuuif
ePeon7aQdl55eHauNslHSooo6TP
a1JUaeWlpeGoCIAa8w
CQ7
F4eG8aAUl9uWmexap1
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
iieeOOfFiixdVgeeiioordoop8aayYG5ee1yuueeJii
nTaauuPeeuueeTeeuueenBooDTIIyiivoooomzeeuuAA
eeDuuuuiif
eePeeoon7aaQdl55eeHaauuNslHSoooooo6TP
aa1JUUaaeeWlpeeGooCIIAAaa8w
CQ7
F4eeG8aaAAUUl9uuWmeexaap1
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
x
NDoo6uGeIepehiSuDteDolSu4
er arx7
N5e Yuumap
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
x
NDoooo6uuGeeIIeepeehiiSuuDteeDoolSuu4
eer aarx7
N5ee Yuuuumaap
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
ocGoi
ucpeHVrwINsuQlueuYepu
xhao1ehm OzLZ3e367Mli0ooGea
eeI5WCAyaeV3WadGoeyugoaF6tFoGg
Weiaiia7QEikoo
Ys08iERuaOEz
gB qmej
uioeMLYq6pNiHyiu9Pnec
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
oocGooii
uucpeeHVrwIINsuuQluueeuuYeepuu
xhaaoo1eehm OOzLZ3ee367Mlii0ooooGeeaa
eeeeII5WCAAyaaeeV3WaadGooeeyuugooaaF6tFooGg
Weeiiaaiiiiaa7QEEiikoooo
Ys08iiEERuuaaOOEEz
gB qmeej
uuiiooeeMLYq6pNiiHyiiuu9Pneec
```
