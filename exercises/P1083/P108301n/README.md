# `P108301n` - Minyonok (`n` teszteset)

## A feladat leírása
A minyonok története az idők kezdetétől ered. A minyonok sárga egysejtű organizmusként kezdték, és fejlődtek a korokon át, és mindig a leggrúsabb gazdákat szolgálták. Mivel ezeket a gazdákat – a T-Rextől Napóleonig – folytonosan elveszítették, a minyonoknak most nincs kit szolgálniuk, és mély depresszióba zuhantak.

Ebben a feladatban minyonok adatait kell beolvasnod a standard inputról, rendezni, majd kiírni a standard outputra.

## Formátumok

* A standard bemeneten egy minyon a következő formátumban szerepel:

    ```
    <minyon_neve>;<éhség>;<lelkesedés>;<nadrág_mérete>
    ```

* A standard kimeneten egy minyon a következő formátumban szerepel:

    ```
    <minyon_neve> <éhség> (<nadrág_mérete>)
    ```

* A jelölések:
  * `minyon_neve`: egy legfeljebb `30` karakter hosszú, csak angol betűket tartalmazó egyedi sztring
  * `éhség`: egy nemnegatív egész érték
  * `lelkesedés`: egy nemnegatív egész érték
  * `nadrág_mérete`: az `"S"`, `"L"`, `"XL"` és "`XXL`" sztringek egyike

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

| `entries` | Visszaadott érték |
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

| `entries` | Visszaadott érték |
| --- | --- |
| `Minion(name='Bob', hunger=87, motivation=100, size='S')` | `"Bob 87 (S)"`
| `Minion(name='Stuart', hunger=50, motivation=30, size='L')` | `"Stuart 50 (L)"`
| `Minion(name='Jerry', hunger=40, motivation=20, size='XL')` | `"Jerry 40 (XL)"`
| `Minion(name='Dave', hunger=43, motivation=10, size='L')` | `"Dave 43 (L)"`

## A(z) `sort_minions` függvény

Írj egy `sort_minions` nevű függvényt, mely megkap egy `Minion` listát, majd rendezi és visszaadja azt!

### Paraméterlista

1. `minions` - a(z) `Minion` elemeket tartalmazó lista

### Visszaadott érték

* a paraméterként megkapott `minions` lista a következő szempontok szerint rendezve:

	1. a lelkesedés szerint csökkenő sorrend
	1. a név szerint növekvő sorrend

### Példák

| `entries` | Visszaadott érték |
| --- | --- |
| `[Minion(name='Bob', hunger=87, motivation=100, size='S'), Minion(name='Dave', hunger=43, motivation=10, size='L'), Minion(name='Stuart', hunger=50, motivation=30, size='L'), Minion(name='Jerry', hunger=40, motivation=20, size='XL')]` | `[Minion(name='Bob', hunger=87, motivation=100, size='S'), Minion(name='Stuart', hunger=50, motivation=30, size='L'), Minion(name='Jerry', hunger=40, motivation=20, size='XL'), Minion(name='Dave', hunger=43, motivation=10, size='L')]` |

## A főprogram

Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemenet sorai egy-egy `Minion` pontosvesszőkkel (`;`) elválasztott adatait tartalmazzák.
* A standard bemenet első sora tartalmazza a feldolgozandó sorok számát (`n`).
* Az első sort pontosan `n` darab, a feladat szövegének megfelelő sor követi.
* A beolvasott sorok feldolgozása a következő módon történik:
	1. a(z) `Minion` lista előállítása a(z) `line_to_minion()` függvény felhasználásával
	1. a(z) `Minion` lista rendezése a(z) `sort_minions()` függvénnyel
	1. a(z) `Minion` lista kiírása a(z) `minion_to_line()` függvény felhasználásával

## Megjegyzés a *C* nyelvű megoldásokhoz

* A rendezéshez a `qsort()` függvényt használd.
* A(z) `minion_to_line()` függvény a `qsort()` függvény negyedik paramétereként megadható, összehasonlító függvény.
* Minden dinamikusan foglalt területet fel kell szabadítani.
* A bemenet egyik sora sem hosszabb `1000` karakternél.
* A bemeneten legfeljebb `20` rekordot leíró sorra kell számítani.

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
Bob 87 (S)
Stuart 50 (L)
Jerry 40 (XL)
Dave 43 (L)
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
J 37 (L)
E 54 (XL)
A 1 (S)
G 35 (XXL)
K 10 (L)
D 80 (XXL)
F 12 (XL)
H 21 (XXL)
B 45 (S)
I 1 (M)
C 26 (L)
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
A 97 (XXL)
H 21 (XL)
E 50 (S)
K 61 (XXL)
B 51 (L)
C 100 (L)
F 30 (XL)
D 75 (S)
I 53 (XXL)
G 54 (L)
J 62 (M)
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
D 54 (S)
J 5 (XL)
C 48 (L)
G 26 (S)
B 79 (M)
A 97 (M)
I 37 (M)
F 37 (XL)
H 76 (M)
E 8 (XL)
```
