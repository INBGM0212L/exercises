# `P104301n` - Lista szorzása (`n` teszteset)

## A függvény
Írj egy `apply_multiplication` nevű függvényt, mely visszaadja azt a listát, melyet úgy kapunk, hogy a `numbers` lista minden elemét megszorozzuk a `multiplier` paraméter értékkel!


### Paraméterlista
1. `numbers` - az eredeti lista (egy legalább `1`, legfeljebb `10` elemből álló egész lista, melynek minden eleme legalább `-99`, legfeljebb `99`)
2. `multiplier` - a szorzó tag (egész érték a(z) `[-1000,1000]` intervallumból)

### Visszaadott érték
* a művelet elvégzésével előálló új lista

### Példák
 | `numbers` | `multiplier` | Visszaadott érték |
 | :--- | :--- | :-- |
 | `[-74]` | `379` | `[-28046]` |
 | `[-76, 86, 47, 37]` | `240` | `[-18240, 20640, 11280, 8880]` |
 | `[-77, 27, -30, -7, -46, 10, 42]` | `-135` | `[10395, -3645, 4050, 945, 6210, -1350, -5670]` |
 | `[77, 72, 66, -23, -62, 96, 62]` | `488` | `[37576, 35136, 32208, -11224, -30256, 46848, 30256]` |
 | `[13, -18, -84, 32, -56, -49, 81, -4, 47, -77]` | `134` | `[1742, -2412, -11256, 4288, -7504, -6566, 10854, -536, 6298, -10318]` |
 | `[84, -43, -25, 28, -2, -85, 61]` | `343` | `[28812, -14749, -8575, 9604, -686, -29155, 20923]` |
 | `[-68, 95]` | `952` | `[-64736, 90440]` |
 | `[-59, 67, 60, -35, -53, 30]` | `152` | `[-8968, 10184, 9120, -5320, -8056, 4560]` |
 | `[-62, 69, 20, -58]` | `521` | `[-32302, 35949, 10420, -30218]` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemeneten legalább `3`, legfeljebb `10` darab teszteset található.
* A tesztesetek száma az első sorban szereplő egész érték.

## Megjegyzés a *C* nyelvű megoldásokhoz
* A bemenet egyetlen sora sem hosszabb `1000` karakternél.
* A függvény `numbers` paramétere az egész számokat tartalmazó tömb kezdőcíme.
* A függvény egy harmadik, `length` nevű (egész típusú) paramétert is megkap, mely a `numbers` tömb méretét tartalmazza.
* A függvény egy dinamikusan foglalt tömb kezdőcímét adja vissza. A tömb végét egy extra, `INT_MIN` értékű elem jelzi.
* A főprogram felszabadítja a tömb mögött álló memóriaterületet.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |
| `test-03` | [`test-03.in`](test-03.in) | [`test-03.out`](test-03.out) |

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
9
-74
379
-76 86 47 37
240
-77 27 -30 -7 -46 10 42
-135
77 72 66 -23 -62 96 62
488
13 -18 -84 32 -56 -49 81 -4 47 -77
134
84 -43 -25 28 -2 -85 61
343
-68 95
952
-59 67 60 -35 -53 30
152
-62 69 20 -58
521
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
-28046
-18240 20640 11280 8880
10395 -3645 4050 945 6210 -1350 -5670
37576 35136 32208 -11224 -30256 46848 30256
1742 -2412 -11256 4288 -7504 -6566 10854 -536 6298 -10318
28812 -14749 -8575 9604 -686 -29155 20923
-64736 90440
-8968 10184 9120 -5320 -8056 4560
-32302 35949 10420 -30218
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
9
81 36 80 -33
-493
35 82 1 74 77 54 68 -55 -54
-505
-15 1 -82 -3 90 -62 -86 88
-652
67
69
69
-213
12 -55 -39 -13 40
501
50 -92 -92 67 70 -52 89 50
402
-65 49
850
73 62 99 -72 97 72
678
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
-39933 -17748 -39440 16269
-17675 -41410 -505 -37370 -38885 -27270 -34340 27775 27270
9780 -652 53464 1956 -58680 40424 56072 -57376
4623
-14697
6012 -27555 -19539 -6513 20040
20100 -36984 -36984 26934 28140 -20904 35778 20100
-55250 41650
49494 42036 67122 -48816 65766 48816
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
8
-16 8 66 92 18 30 -22
575
-65 89 4
-281
81 82 21 -6 -27 -68 80 -49
964
99 -64
284
-7 39 57 84 -60
-397
48 8
-533
71 -72 88 -21 -7 68
757
61 -33 49 24 -70 85 -96 66 -16
-758
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
-9200 4600 37950 52900 10350 17250 -12650
18265 -25009 -1124
78084 79048 20244 -5784 -26028 -65552 77120 -47236
28116 -18176
2779 -15483 -22629 -33348 23820
-25584 -4264
53747 -54504 66616 -15897 -5299 51476
-46238 25014 -37142 -18192 53060 -64430 72768 -50028 12128
```
