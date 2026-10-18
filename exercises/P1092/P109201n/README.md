# `P109201n` - Minyonok (`n` teszteset)

## A feladat leírása
A minyonok története az idők kezdetétől ered. A minyonok sárga egysejtű organizmusként kezdték, és fejlődtek a korokon át, és mindig a leggrúsabb gazdákat szolgálták. Mivel ezeket a gazdákat – a T-Rextől Napóleonig – folytonosan elveszítették, a minyonoknak most nincs kit szolgálniuk, és mély depresszióba zuhantak.

Ebben a feladatban minyonok adatai kell beolvasnod a standard inputról, majd feldolgozni a beolvasott listát.

## Formátumok

* A standard bemeneten egy minyon a következő formátumban szerepel:

    ```
    minyon_neve;éhség;lelkesedés;nadrág_mérete
    ```

* A standard kimeneten egy minyon a következő formátumban szerepel:

    ```
    minyon_neve éhség (nadrág_mérete)
    ```

* A jelölések:

  * A `minyon_neve` egy legfeljebb `30` karakter hosszú, csak angol betűket tartalmazó egyedi sztring.
  * Az `éhség` és a `lelkesedés` egyaránt `0` és `100` közötti egész szám.
  * A `nadrág_mérete` az `"S"`, `"L"`, `"XL"` és "`XXL`" sztringek egyike.

A feladat megoldását több függvényre kell bontanod, ezek leírását egyenként, lentebb találod.

## A(z) `Minion` típus
Definiáld a `Minion` nevű nevesített tuple-t, mely a következő mezőkkel rendelkezik:

* `name`: a minyon neve (típus: `<class 'str'>`)
* `hunger`: a minyon éhsége (típus: `<class 'int'>`)
* `motivation`: a minyon motiváltsága (típus: `<class 'int'>`)
* `size`: a minyon mérete (típus: `<class 'str'>`)

## A(z) `line_to_minion` függvény
Írj egy `line_to_minion` nevű függvényt, mely megkapja a bemenet egy sorát, majd visszaadja sorból kinyert adatokkal feltöltött, `Minion` *nevesített tuple*-t!

### Paraméterlista

1. a bemenet egy `Minion` rekordot leíró sora

### Visszaadott érték

* a `line` paraméternek megfelelő `Minion` rekord

### Példák

| `line` | Visszaadott érték |
| --- | --- |
| `"Bob;87;100;S"` | `Minion(name='Bob', hunger=87, motivation=100, size='S')` |
| `"Dave;43;10;L"` | `Minion(name='Dave', hunger=43, motivation=10, size='L')` |
| `"Stuart;50;30;L"` | `Minion(name='Stuart', hunger=50, motivation=30, size='L')` |
| `"Jerry;40;20;XL"` | `Minion(name='Jerry', hunger=40, motivation=20, size='XL')` |

## A(z) `count_by_sizes` függvény

Írj egy `count_by_sizes` nevű függvényt, mely visszaadja azt, hogy a `minions` paraméterben az egyes nadrágméreteket hány minyon viseli!

### Paraméterlista

1. `minions` - a(z) `Minion` elemeket tartalmazó lista (típusa: `list[Minion]`)

### Visszaadott érték

* egy szótár, melynek a kulcsai nadrágméretek, egy-egy értéke pedig az adott nadrágméretet viselő minyonok száma (típusa: `dict[str, int]`)


### Példák

| `minions` | Visszaadott érték |
| --- | --- |
| `[Minion(name='Bob', hunger=87, motivation=100, size='S'), Minion(name='Dave', hunger=43, motivation=10, size='L'), Minion(name='Stuart', hunger=50, motivation=30, size='L'), Minion(name='Jerry', hunger=40, motivation=20, size='XL')]` | `{'S': 1, 'L': 2, 'XL': 1}` |

## A főprogram

Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemenet sorai egy-egy `Minion` pontosvesszőkkel (`;`) elválasztott adatait tartalmazzák.
* A standard bemenet első sora tartalmazza a feldolgozandó sorok számát (`n`).
* Az első sort pontosan `n` darab, a feladat szövegének megfelelő sor követi.
* A beolvasott sorok feldolgozása a következő módon történik:
	1. A(z) `Minion` lista előállítása a(z) `line_to_minion()` függvény felhasználásával.
	1. A(z) `count_by_sizes()` függvény meghívása.
	1. A visszakapott szótár bejegyzéseinek kiírása. Minden bejegyzés egy külön, `<kulcs>: <érték>` formátumú sorba kerüljön, ahol a `kulcs` a szótár egy kulcsa, az `érték` pedig a kulcshoz tartozó érték.

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
4
Bob;87;100;S
Dave;43;10;L
Stuart;50;30;L
Jerry;40;20;XL
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
S: 1
L: 2
XL: 1
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
11
I;1;27;M
C;26;2;L
G;35;79;XXL
D;80;34;XXL
F;12;32;XL
E;54;95;XL
B;45;27;S
H;21;29;XXL
K;10;55;L
J;37;99;L
A;1;83;S
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
M: 1
L: 3
XXL: 3
XL: 2
S: 2
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
11
F;30;46;XL
I;53;31;XXL
G;54;21;L
H;21;71;XL
A;97;73;XXL
J;62;18;M
B;51;60;L
C;100;59;L
K;61;67;XXL
E;50;67;S
D;75;34;S
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
XL: 2
XXL: 3
L: 3
M: 1
S: 2
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
10
E;8;12;XL
J;5;77;XL
G;26;66;S
D;54;98;S
F;37;16;XL
I;37;22;M
A;97;24;M
B;79;57;M
H;76;13;M
C;48;69;L
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
XL: 3
S: 2
M: 4
L: 1
```
