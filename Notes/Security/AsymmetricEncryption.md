## Explanation

**Asymmetric encryption** (also called **public-key cryptography**) uses **two different keys**:
- A **public key** for encryption.  
- A **private key** for decryption.  

The two keys are mathematically related, but it is computationally infeasible to derive one from the other.

Encryption:  Ciphertext = Encrypt(PublicKey, Plaintext)  
Decryption:  Plaintext = Decrypt(PrivateKey, Ciphertext)

Only the holder of the private key can decrypt messages encrypted with the public key.

## Characteristics

- **Key pair:** one public, one private.  
- Public key can be shared openly; private key must be kept secret.  
- Solves the **key distribution problem** of symmetric encryption.  

## Common Algorithms

1. **RSA (Rivest–Shamir–Adleman):**  
   Based on difficulty of factoring large integers; widely used.  

2. **ECC (Elliptic Curve Cryptography):**  
   Based on elliptic curve mathematics; provides same security with smaller keys.  

3. **DSA (Digital Signature Algorithm):**  
   Used for authentication and digital signatures.  

4. **ElGamal:**  
   Based on discrete logarithm problem; used in some hybrid encryption systems.  

5. **Diffie–Hellman Key Exchange:**  
   Used to securely exchange symmetric keys over an insecure channel.  

## Advantages

- Eliminates need for secure key exchange.  
- Enables **digital signatures** (authentication + integrity).  
- Provides both **confidentiality** and **non-repudiation**.

## Disadvantages

- Much slower than symmetric encryption.  
- Higher computational cost (especially for large data).  
- Typically used only to encrypt small pieces of data (like session keys).  

## Applications / Use Cases

- Secure key exchange (e.g., HTTPS handshake).  
- Digital signatures and certificates.  
- Secure email (PGP, S/MIME).  
- Authentication and identity verification.  
- Blockchain and cryptocurrency transactions.  

## Key Points / Notes

- In practice, asymmetric encryption is combined with symmetric encryption (hybrid approach):  
  - Asymmetric encryption secures the **key**.  
  - Symmetric encryption secures the **data**.  

- **Public Key Infrastructure (PKI)** manages key distribution, verification, and trust.  
- Private key must be stored securely; compromise leads to loss of confidentiality and authenticity.  
- ECC is preferred for modern systems due to shorter keys and faster performance.  
