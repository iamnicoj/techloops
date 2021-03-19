``` java
0110 + 0010 = 1000
0011 * 0101 = 1111
            0011
            0
            11
            0 
0110 + 0110 = 1100 // power of 2, shift left 
0011 + 0010 = 0101 
0011 * 0011 = 0011 + 00110 = 1001
0100 * 0011 = 1100 // * by 4 is left shift by 2
0110 - 0011 = 0101 - 10 = 0011
1101 >> 2   = 0011

^ XOR 
~ NOT 
& AND  = Multiplication 1 * 1 = 1 0 Otherwise
OR     = 1 or 1 = 1; 1 or 0 = 1; 0 or 0 = 0

1101 ^ (~1101)   = 1101 ^ 0010 = 1111 // XOR by opositve is 1
1000 - 0110      = 0010
1101 ^ 0101      = 1000
1011 & (~0 << 2) = 1011 & 0100 = 0000

```

`asdfsadf`

When shifting left, the most-significant bit is lost, and a 00 bit is inserted on the other end.

The left shift operator is usually written as "<<".

> 0010 << 1  →  0100
> 0010 << 2  →  1000

A single left shift multiplies a binary number by 2:

>  0010 << 1  →  0100
> 0010 is 2
> 0100 is 4

```
X ^ 0s  = X
X ^ 1s  = ~X
X ^ X   = 0

X & 0s  = 0
X & 1s  = X  
X & X   = X

X | 0s  = x
X | 1s  = 1s
X | X   = x
```

