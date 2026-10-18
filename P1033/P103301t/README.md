# `P103301t` - Rekurzív `n` faktoriális (végjelig olvasás)

## A függvény
Írj egy `n_factorial` nevű függvényt, mely visszaadja az `n!` értékét! A függvény rekurzív módon határozza meg az eredményt!


### Paraméterlista
1. `n` - az `n` értéke (egész érték a(z) `[0,50]` intervallumból)

### Visszaadott érték
* az `n!` értéke

### Példák
 | `n` | Visszaadott érték |
 | :--- | :-- |
 | `44` | `2658271574788448768043625811014615890319638528000000000` |
 | `16` | `20922789888000` |
 | `41` | `33452526613163807108170062053440751665152000000000` |
 | `33` | `8683317618811886495518194401280000000` |
 | `0` | `1` |
 | `28` | `304888344611713860501504000000` |
 | `41` | `33452526613163807108170062053440751665152000000000` |
 | `46` | `5502622159812088949850305428800254892961651752960000000000` |
 | `11` | `39916800` |


## A főprogram
Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* Minden tesztesetet pontosan egy sor ír le, melyben a függvény argumentuma (`n`) szerepel.

## Megjegyzés a *C* nyelvű megoldásokhoz
A példákban látható értékeket egy *Python* nyelvű megoldás állította elő. A *C* nyelv típusaival nem ábrázolható az összes példákban szereplő érték.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |
| `test-03` | [`test-03.in`](test-03.in) | [`test-03.out`](test-03.out) |

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
44
16
41
33
0
28
41
46
11
-1
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
2658271574788448768043625811014615890319638528000000000
20922789888000
33452526613163807108170062053440751665152000000000
8683317618811886495518194401280000000
1
304888344611713860501504000000
33452526613163807108170062053440751665152000000000
5502622159812088949850305428800254892961651752960000000000
39916800
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
3
40
29
21
14
19
31
-1
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
6
815915283247897734345611269596115894272000000000
8841761993739701954543616000000
51090942171709440000
87178291200
121645100408832000
8222838654177922817725562880000000
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
6
41
37
9
34
5
9
-1
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
720
33452526613163807108170062053440751665152000000000
13763753091226345046315979581580902400000000
362880
295232799039604140847618609643520000000
120
362880
```
