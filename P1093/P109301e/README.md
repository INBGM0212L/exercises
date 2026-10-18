# `P109301e` - Minyonok (állományvégjelig olvasás)

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

## A(z) `minion_to_line` függvény

Írj egy `minion_to_line` nevű függvényt, mely megkap egy `Minion` rekordot, majd visszaadja a neki megfelelő, kimenetre írható sztringet!

### Paraméterlista

1. `minion` - a(z) `Minion` típusú rekord

### Visszaadott érték

* az `minion` paraméternek megfelelő sztring reprezentáció

### Példák

| `minion` | Visszaadott érték |
| --- | --- |
| `Minion(name='Bob', hunger=87, motivation=100, size='S')` | `"Bob 87 (S)"`
| `Minion(name='Dave', hunger=43, motivation=10, size='L')` | `"Dave 43 (L)"`
| `Minion(name='Stuart', hunger=50, motivation=30, size='L')` | `"Stuart 50 (L)"`
| `Minion(name='Jerry', hunger=40, motivation=20, size='XL')` | `"Jerry 40 (XL)"`

## A(z) `group_by_sizes` függvény

Írj egy `group_by_sizes` nevű függvényt, mely nadrágméretenként csoportosítja a `minions` paraméterben szereplő minyonokat!

### Paraméterlista

1. `minions` - a(z) `Minion` elemeket tartalmazó lista (típusa: `list[Minion]`)

### Visszaadott érték

* egy szótár, melynek a kulcsai nadrágméretek, egy-egy értéke pedig az adott nadrágméretet viselő minyonok listája (típusa: `dict[str, list[Minion]]`)


### Példák

| `minions` | Visszaadott érték |
| --- | --- |
| `[Minion(name='Bob', hunger=87, motivation=100, size='S'), Minion(name='Dave', hunger=43, motivation=10, size='L'), Minion(name='Stuart', hunger=50, motivation=30, size='L'), Minion(name='Jerry', hunger=40, motivation=20, size='XL')]` | `{'S': [Minion(name='Bob', hunger=87, motivation=100, size='S')], 'L': [Minion(name='Dave', hunger=43, motivation=10, size='L'), Minion(name='Stuart', hunger=50, motivation=30, size='L')], 'XL': [Minion(name='Jerry', hunger=40, motivation=20, size='XL')]}` |

## A főprogram

Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemenet sorai egy-egy `Minion` pontosvesszőkkel (`;`) elválasztott adatait tartalmazzák.
* A tesztesetek végét állományvégjel (`EOF`) jelzi.
* A beolvasott sorok feldolgozása a következő módon történik:
	1. A(z) `Minion` lista előállítása a(z) `line_to_minion()` függvény felhasználásával.
	1. A(z) `group_by_sizes()` függvény meghívása.
	1. A visszakapott szótár bejegyzéseinek kiírása.
		* Először a bejegyzés kulcsa kerül a kimenetre, egy külön sorba.
		* Ezt követik a kulcshoz tartozó lista elemei, soronként pontosan egy. Minden `Minion` rekord a(z) `minion_to_line()` függvény segítségével kerül kiírásra.

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
Bob;87;100;S
Dave;43;10;L
Stuart;50;30;L
Jerry;40;20;XL
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
S
Bob 87 (S)
L
Dave 43 (L)
Stuart 50 (L)
XL
Jerry 40 (XL)
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
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
M
I 1 (M)
L
C 26 (L)
K 10 (L)
J 37 (L)
XXL
G 35 (XXL)
D 80 (XXL)
H 21 (XXL)
XL
F 12 (XL)
E 54 (XL)
S
B 45 (S)
A 1 (S)
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
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
XL
F 30 (XL)
H 21 (XL)
XXL
I 53 (XXL)
A 97 (XXL)
K 61 (XXL)
L
G 54 (L)
B 51 (L)
C 100 (L)
M
J 62 (M)
S
E 50 (S)
D 75 (S)
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
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
XL
E 8 (XL)
J 5 (XL)
F 37 (XL)
S
G 26 (S)
D 54 (S)
M
I 37 (M)
A 97 (M)
B 79 (M)
H 76 (M)
L
C 48 (L)
```
