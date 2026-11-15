# Crypto — Cheatsheet

## Encoding vs encryption
- base64: `echo -n x | base64 -d`
- hex: `xxd -r -p`
- ROT13: `tr 'A-Za-z' 'N-ZA-Mn-za-m'`
- CyberChef for chains

## Classical
- Caesar / Vigenere / Substitution: dcode.fr or quipqiup
- Frequency analysis beats substitution

## XOR
- Reused key = crib drag; look for known plaintext (flag{, CTF{)

## RSA
- n = p*q; phi = (p-1)(q-1); d = inverse(e, phi)
- Small e (e=3) + short message: m = c^(1/3)
- Factor small n with factordb.com / sympy.factorint

## Symmetric
- ECB = identical plaintext blocks give identical ciphertext
- CBC padding oracle = flip padding to leak bytes

## Tools
- sage, sympy, pycryptodome, CyberChef, factordb
