# `P109302t` - Hullámvasutak (végjelig olvasás)

## A feladat leírása
Egy zsúfolt vidámparkban olykor több órát is sorban kell ahhoz állni, hogy felülhessünk egy-egy hullámvasútra. A parkok méretére és a kígyózó sorokra való tekintettel érdemes megtervezni, hogy milyen sorrendben ülünk fel a játékaikra. A [PortAventura World](https://www.portaventuraworld.com/en) Európa egyik legnagyobb vidámparkja, mely a Costa Braván, Salou és Tarragona között található. Klasszikus területe (a kontinens egyetlen Ferrari parkján kívül) több tematikus világot tartalmaz, amelyek mindegyikében található legalább egy hullámvasút.

Ebben a feladatban hullámvasutak adatait kell beolvasnod a standard inputról, majd feldolgozni a beolvasott listát.

## Formátumok

* A standard bemeneten egy hullámvasút a következő formátumban szerepel:
    ```
    <hullámvasút_neve>;<világ_neve>;<legkisebb_magasság>;<várakozási_idő>
    ```

* A standard kimeneten egy hullámvasút a következő formátumban szerepel:
    ```
    <hullámvasút_neve> (<világ_neve>): <várakozási_idő>
    ```

* A jelölések:
  * `hullámvasút_neve`: egy legfeljebb `30` karakter hosszú, csak angol betűket és szóközöket tartalmazó egyedi sztring
  * `világ_neve`: egy legfeljebb `30` karakter hosszú, csak angol betűket és szóközöket tartalmazó egyedi sztring
  * `legkisebb_magasság`: egy nemnegatív egész érték
  * `várakozási_idő`: egy nemnegatív egész érték

A feladat megoldását több függvényre kell bontanod, ezek leírását egyenként, lentebb találod.

## A(z) `RollerCoaster` típus
Definiáld a `RollerCoaster` nevű nevesített tuple-t, mely a következő mezőkkel rendelkezik:

* `name`: a hullámvasút neve (típus: `<class 'str'>`)
* `world`: a világ neve (típus: `<class 'str'>`)
* `height`: a legkisebb magasság (típus: `<class 'int'>`)
* `time`: a várakozási idő (típus: `<class 'int'>`)

## A(z) `line_to_coaster` függvény
Írj egy `line_to_coaster` nevű függvényt, mely megkapja a bemenet egy sorát, majd visszaadja sorból kinyert adatokkal feltöltött, `RollerCoaster` *nevesített tuple*-t!

### Paraméterlista

1. a bemenet egy `RollerCoaster` rekordot leíró sora

### Visszaadott érték

* a `line` paraméternek megfelelő `RollerCoaster` rekord

### Példák

| `line` | Visszaadott érték |
| --- | --- |
| `"Furius baco;Polynesia;140;120"` | `RollerCoaster(name='Furius baco', world='Polynesia', height=140, time=120)` |
| `"Shambhala;China;140;120"` | `RollerCoaster(name='Shambhala', world='China', height=140, time=120)` |
| `"Dragon Khan;China;140;80"` | `RollerCoaster(name='Dragon Khan', world='China', height=140, time=80)` |
| `"Stampida;Far West;120;20"` | `RollerCoaster(name='Stampida', world='Far West', height=120, time=20)` |
| `"Tami Tami;SesamoAventura;100;20"` | `RollerCoaster(name='Tami Tami', world='SesamoAventura', height=100, time=20)` |
| `"El Diablo;Mexico;140;30"` | `RollerCoaster(name='El Diablo', world='Mexico', height=140, time=30)` |

## A(z) `coaster_to_line` függvény

Írj egy `coaster_to_line` nevű függvényt, mely megkap egy `RollerCoaster` rekordot, majd visszaadja a neki megfelelő, kimenetre írható sztringet!

### Paraméterlista

1. `coaster` - a(z) `RollerCoaster` típusú rekord

### Visszaadott érték

* az `coaster` paraméternek megfelelő sztring reprezentáció

### Példák

| `coaster` | Visszaadott érték |
| --- | --- |
| `RollerCoaster(name='Furius baco', world='Polynesia', height=140, time=120)` | `"Furius baco (Polynesia): 120"`
| `RollerCoaster(name='Shambhala', world='China', height=140, time=120)` | `"Shambhala (China): 120"`
| `RollerCoaster(name='Dragon Khan', world='China', height=140, time=80)` | `"Dragon Khan (China): 80"`
| `RollerCoaster(name='Stampida', world='Far West', height=120, time=20)` | `"Stampida (Far West): 20"`
| `RollerCoaster(name='Tami Tami', world='SesamoAventura', height=100, time=20)` | `"Tami Tami (SesamoAventura): 20"`
| `RollerCoaster(name='El Diablo', world='Mexico', height=140, time=30)` | `"El Diablo (Mexico): 30"`

## A(z) `group_by_worlds` függvény

Írj egy `group_by_worlds` nevű függvényt, mely világonként csoportosítja a `coasters` paraméterként megkapott hullámvasutakat!

### Paraméterlista

1. `coasters` - a(z) `RollerCoaster` elemeket tartalmazó lista (típusa: `list[RollerCoaster]`)

### Visszaadott érték

* egy szótár, melynek a kulcsai világok nevei, egy-egy értéke pedig az adott világhoz tartozó hullámvasutak listája (típusa: `dict[str, list[RollerCoaster]]`)


### Példák

| `coasters` | Visszaadott érték |
| --- | --- |
| `[RollerCoaster(name='Furius baco', world='Polynesia', height=140, time=120), RollerCoaster(name='Shambhala', world='China', height=140, time=120), RollerCoaster(name='Dragon Khan', world='China', height=140, time=80), RollerCoaster(name='Stampida', world='Far West', height=120, time=20), RollerCoaster(name='Tami Tami', world='SesamoAventura', height=100, time=20), RollerCoaster(name='El Diablo', world='Mexico', height=140, time=30)]` | `{'Polynesia': [RollerCoaster(name='Furius baco', world='Polynesia', height=140, time=120)], 'China': [RollerCoaster(name='Shambhala', world='China', height=140, time=120), RollerCoaster(name='Dragon Khan', world='China', height=140, time=80)], 'Far West': [RollerCoaster(name='Stampida', world='Far West', height=120, time=20)], 'SesamoAventura': [RollerCoaster(name='Tami Tami', world='SesamoAventura', height=100, time=20)], 'Mexico': [RollerCoaster(name='El Diablo', world='Mexico', height=140, time=30)]}` |

## A főprogram

Készíts egy olyan főprogramot, mely az alábbi specifikációk alapján teszi kipróbálhatóvá a megoldást!

* A standard bemenet sorai egy-egy `RollerCoaster` pontosvesszőkkel (`;`) elválasztott adatait tartalmazzák.
* A tesztesetek végét a következő sor jelzi (melyet már nem kell feldolgozni): `"END"`.
* A beolvasott sorok feldolgozása a következő módon történik:
	1. A(z) `RollerCoaster` lista előállítása a(z) `line_to_coaster()` függvény felhasználásával.
	1. A(z) `group_by_worlds()` függvény meghívása.
	1. A visszakapott szótár bejegyzéseinek kiírása.
		* Először a bejegyzés kulcsa kerül a kimenetre, egy külön sorba.
		* Ezt követik a kulcshoz tartozó lista elemei, soronként pontosan egy. Minden `RollerCoaster` rekord a(z) `coaster_to_line()` függvény segítségével kerül kiírásra.

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
Furius baco;Polynesia;140;120
Shambhala;China;140;120
Dragon Khan;China;140;80
Stampida;Far West;120;20
Tami Tami;SesamoAventura;100;20
El Diablo;Mexico;140;30
END
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
Polynesia
Furius baco (Polynesia): 120
China
Shambhala (China): 120
Dragon Khan (China): 80
Far West
Stampida (Far West): 20
SesamoAventura
Tami Tami (SesamoAventura): 20
Mexico
El Diablo (Mexico): 30
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
E;V;1;170
K;C;4;97
C;T;2;55
A;F;4;278
G;V;2;74
B;O;2;148
F;H;3;164
D;J;1;129
H;I;2;83
J;B;3;135
I;R;4;130
END
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
V
E (V): 170
G (V): 74
C
K (C): 97
T
C (T): 55
F
A (F): 278
O
B (O): 148
H
F (H): 164
J
D (J): 129
I
H (I): 83
B
J (B): 135
R
I (R): 130
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
H;F;2;176
E;C;2;192
I;H;2;189
C;U;2;161
A;K;4;134
B;T;3;178
D;H;2;115
J;M;3;284
F;X;1;198
G;V;4;269
END
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
F
H (F): 176
C
E (C): 192
H
I (H): 189
D (H): 115
U
C (U): 161
K
A (K): 134
T
B (T): 178
M
J (M): 284
X
F (X): 198
V
G (V): 269
```

### `test-03`

#### Standard bemenet ([`test-03.in`](test-03.in))

```
H;U;4;177
B;F;3;185
J;D;3;191
L;Y;4;162
D;L;2;185
G;T;1;93
E;Y;4;265
A;M;2;290
F;S;4;231
P;D;3;138
N;V;2;203
I;H;1;152
M;K;3;268
C;R;4;187
R;K;4;85
Q;F;3;264
O;H;2;189
K;M;2;252
END
```

#### Elvárt kimenet ([`test-03.out`](test-03.out))

```
U
H (U): 177
F
B (F): 185
Q (F): 264
D
J (D): 191
P (D): 138
Y
L (Y): 162
E (Y): 265
L
D (L): 185
T
G (T): 93
M
A (M): 290
K (M): 252
S
F (S): 231
V
N (V): 203
H
I (H): 152
O (H): 189
K
M (K): 268
R (K): 85
R
C (R): 187
```
