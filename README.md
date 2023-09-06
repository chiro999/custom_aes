# Coding a 128-bit Galois-Counter Mode AES cipher

## KeyExpansion – round keys are derived from the cipher key using the AES key schedule. AES requires a separate 128-bit round key block for each round plus one more.
## Initial round key addition:
1 . AddRoundKey – each byte of the state is combined with a byte of the round key using bitwise xor.

## 9, 11 or 13 rounds:
### SubBytes – a non-linear substitution step where each byte is replaced with another according to a lookup table.
### ShiftRows – a transposition step where the last three rows of the state are shifted cyclically a certain number of steps.
### MixColumns – a linear mixing operation which operates on the columns of the state, combining the four bytes in each column.
    

## Final round (making 10, 12 or 14 rounds in total):

    SubBytes
    ShiftRows
    AddRoundKey
