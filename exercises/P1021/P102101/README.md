# `P102101` - Aritmetikai műveletek #1

Írjon programot, amely a standard bemenetről egész számokat és a Python programozási nyelv operátorait olvassa soronként, majd a beolvasott értékeken elvégzi az operátor által jelzett műveletet, és a standard kimenetre írja az eredményt!

## A bemenet specifikációja

A bemenet több tesztesetet tartalmaz. A bemenet első sora egy `n` pozitív egész számot tartalmaz, amely a tesztesetek számát jelzi. Az első sort követő sorok mindegyike egy-egy tesztesetet ír le. Minden teszteset egy `x op y` formátumú sor, ahol `x` és `y` egész számok, míg `op` a Python programozási nyelv egész típusú operandusokra alkalmazható alábbi aritmetikai operátorainak egyike: `+`, `-`, `*`, `/`, `//`, `%`. Az operandusok az operátortól egy-egy szóközzel vannak elválasztva.

## A kimenet specifikációja

A programnak minden tesztesetre egy sort kell kiírnia, amely a tesztesetben megadott `x op y` művelet eredményét tartalmazza.

## Megjegyzés `C` nyelvhez

A `//` operátor nem tárolható karakterként, ezért helyette használd a `'~'` karaktert.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-00` | [`test-00.in`](test-00.in) | [`test-00.out`](test-00.out) |

### `test-00`

#### Standard bemenet ([`test-00.in`](test-00.in))

```
6
5 + -5
165 - -10
-5 * -2
23 / 8
23 // 8
25 % 3
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
0
175
10
2.875
2
1
```
