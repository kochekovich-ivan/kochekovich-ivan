## Statement
If p is a prime number and a is an integer not divisible by p, then:

a^(p−1) ≡ 1 (mod p)

Equivalently:

a^p ≡ a (mod p)

## Meaning
- Raising a to (p−1) and dividing by p always leaves remainder 1.
- Works only when p is prime.

## Example
Let p = 7, a = 3:

3^(7−1) = 3^6 = 729  
729 mod 7 = 1 

So 3^6 ≡ 1 (mod 7).

## Applications
- **Primality testing:** if a^(p−1) mod p ≠ 1 → p is definitely not prime.
- **Modular arithmetic:** used in cryptography (RSA, Diffie–Hellman).
- **Computing modular inverses:**  
  a^(p−2) ≡ a^(−1) (mod p) when p is prime.

## Key Notes
- Does not guarantee p is prime (Carmichael numbers are exceptions).
- Works only when gcd(a, p) = 1 (a and p are coprime).
