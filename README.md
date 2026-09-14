README file for Lab 1
I.Shumskii
CISP310


# Lab 1 — First Contact

## TODO 4 — Little-endian TEMP

The temperature bytes are F2 FF.

Because the data is little-endian, the low byte comes first.
Therefore, the 16-bit word is:

F2 FF → FFF2h

## TODO 5 — Two's complement

TEMP = FFF2h

Binary:

1111 1111 1111 0010

Invert the bits:

0000 0000 0000 1101

Add 1:

0000 0000 0000 1110

000Eh = 14

Because the original value is negative:

FFF2h = -14

## TODO 6 — Battery

Battery bytes:

5E 0F

Because the data is little-endian:

5E 0F → 0F5Eh

Convert to decimal:

0F5Eh = 0 × 4096 + 15 × 256 + 5 × 16 + 14

= 0 + 3840 + 80 + 14

= 3934

Therefore, the battery value is 3934 millivolts.

## Questions

### 1. What is little-endian mode?

Little-endian mode means that when a multi-byte value is stored in memory, the lowest byte is stored first, followed by the higher bytes.

### 2. Why do binary and hexadecimal numbers need a suffix?

The suffix tells the assembler what number system the literal is written in. `b` means binary and `h` means hexadecimal.