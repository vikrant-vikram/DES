


# <a href="https://github.com/vikrant-vikram/Cryptography/blob/main/Assignment/trivium_cipher.py">  *Trivium Cipher* </a>

<a href="https://en.wikipedia.org/wiki/DES_supplementary_material">DES supplementary material</a>


<div align="center">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6a/DES-main-network.png/500px-DES-main-network.png" height="500" />

<pre>

DES (Data Encryption Standard) is a symmetric-key block cipher algorithm developed in the 1970s by IBM and later adopted by the U.S. government as an official standard. Here are key details about DES:
Block Size and Key Length: DES operates on 64-bit blocks of data and uses a 56-bit key (technically 64 bits, but 8 bits are used for parity checking and discarded).
Feistel Network: DES uses a 16-round Feistel network structure, where the data block is split into two 32-bit halves that are processed alternately.
S-boxes: DES employs eight substitution boxes (S-boxes) that perform the core of the cryptographic transformation, introducing non-linearity to the cipher.
Key Schedule: The algorithm generates 16 48-bit subkeys from the original 56-bit key, one for each round of the Feistel network.
Initial and Final Permutations: DES applies initial and final permutations to the data block, which don't contribute to the cryptographic strength but were included for ease of implementation in hardware.
Security: While considered secure when first introduced, DES is now vulnerable to brute-force attacks due to its short key length. It has been largely replaced by more secure algorithms like AES.







Example for Avalanche Property (as you can see there is a difference in only one bit of the plaintext)
Plaintext: 0000000000000000       Key: 22234512987ABB23    Ciphertext: 4789FD476E82A5F1

Plaintext: 0000000000000001       Key: 22234512987ABB23    Ciphertext: 0A4ED5C15A63FEA3


Then in this case you should observe the changes in the following number of bits in each round as described below:
Rounds:                 1    2    3     4    5    6    7    8    9    10    11    12    13    14    15    16
Bit differences:     1   6   20   29  30  33  32  29  32  39    33    28     30    31    30    29
<pre>
