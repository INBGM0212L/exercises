# `P102115` - Osztályozás #2

Írjon programot, amely segít leosztályozni a hallgatók dolgozaton elért eredményeit! A dolgozaton elérhető maximális pontszám 100 pont, továbbá a hallgató érdemjegye

* jeles, ha legalább 80 pontot ért el;
* jó, ha legalább 70 pontot ért el, de nem ért el 80 pontot;
* közepes, ha legalább 60 pontot ért el, de nem ért el 70 pontot;
* elégséges, ha legalább 50 pontot ért el, de nem ért el 60 pontot;
* elégtelen, ha nem ért el 50 pontot.

## A bemenet specifikációja

A bemenet minden sora egy-egy hallgató `0` és `100 `közötti egész pontszámát tartalmazza. A bemenet végét állományvégjel (`EOF`) jelzi.

## A kimenet specifikációja

A programnak minden hallgató esetén pontosan egy sort kell a standard kimenetre írnia, amely az általa elért érdemjegyet tartalmazza ékezetek nélkül, vagyis a `jeles`, a `jo`, a `kozepes`, az `elegseges` valamint az `elegtelen` sztringek egyikét.

## Tesztek

| Teszt | Bemenet | Elvárt kimenet |
| :--- | :--- | :--- |
| `test-00` | [`test-00.in`](test-00.in) | [`test-00.out`](test-00.out) |
| `test-01` | [`test-01.in`](test-01.in) | [`test-01.out`](test-01.out) |
| `test-02` | [`test-02.in`](test-02.in) | [`test-02.out`](test-02.out) |

### `test-00`

#### Standard bemenet ([`test-00.in`](test-00.in))

```
45
90
```

#### Elvárt kimenet ([`test-00.out`](test-00.out))

```
elegtelen
jeles
```

### `test-01`

#### Standard bemenet ([`test-01.in`](test-01.in))

```
80
```

#### Elvárt kimenet ([`test-01.out`](test-01.out))

```
jeles
```

### `test-02`

#### Standard bemenet ([`test-02.in`](test-02.in))

```
88
```

#### Elvárt kimenet ([`test-02.out`](test-02.out))

```
jeles
```
