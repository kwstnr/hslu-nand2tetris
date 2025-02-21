# Notizen Elementare Logikgatter
## Kanonische Darstellung
True werte der Wahrheitstabelle. Minterm (m^x) hat genau für eine Belegung m(x,y,z...) den Wert 1.

Kanonische Darstellung = alle Minterme der Wahrheitstabelle mit AND's zusammenführen.

Beispiel: f(x,y,z) = (x + y) * !z

|x|y|z|f(x,y,z)|m|
|*|*|*|*|*|
|0|0|0|0|m0|
|0|0|1|0|m1|
|0|1|0|1|m2|
|0|1|1|0|m3|
|1|0|0|1|m4|
|1|0|1|0|m5|
|1|1|0|1|m6|
|1|1|1|0|m7|

f(x,y,z) = m2 + m4 + m6 = !x*y*!z + x*!y*!z + x*y*!z

## NAND
!(x*y) = max 1 Bit True/1

Alle drei Operatorn (AND, OR, NOT) können aus NAND gebaut werden.

```
x OR y = x + y = (x NAND x) NAND (y NAND y)

1 OR 0 = 1 + 0 = (1 NAND 1) NAND (0 NAND 0) = 0 NAND 1 = 1
0 OR 0 = 0 + 0 = (0 NAND 0) NAND (0 NAND 0) = 1 NAND 1 = 0
```

## Gatterlogik
AND(a,b,c) = If a=b=c=1 then out=1

Implementierung des Logikgatter:
```
AND(a,b,c)=AND(AND(a,b),c)
```

```
XOR = "=1"
OR = ">=1"
```

Mux = "Multiplexer"

