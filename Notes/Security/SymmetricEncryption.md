## Explanation

**Symmetric encryption** is a cryptographic method where the **same key** is used for both **encryption** (locking data) and **decryption** (unlocking data).  

It transforms plaintext into ciphertext using an algorithm and secret key.  
To recover the original message, the receiver uses the same key with the decryption algorithm.

Encryption:  Ciphertext = Encrypt(Key, Plaintext)  
Decryption:  Plaintext = Decrypt(Key, Ciphertext)

## Characteristics

- Single shared secret key.  
- Fast and efficient for large data volumes.  
- Requires secure key exchange between sender and receiver.

## Common Algorithms

1. **DES (Data Encryption Standard):**  
   56-bit key; now considered insecure.

2. **3DES (Triple DES):**  
   Applies DES three times; more secure than DES but slower.

3. **AES (Advanced Encryption Standard):**  
   Block cipher with key sizes 128, 192, 256 bits; widely used standard.

4. **Blowfish / Twofish:**  
   Variable key length; good balance between speed and security.

5. **RC4 (Rivest Cipher 4):**  
   Stream cipher; now deprecated due to vulnerabilities.

6. **ChaCha20:**  
   Modern stream cipher, secure and fast alternative to RC4.

## Advantages

- High speed and efficiency.  
- Suitable for encrypting large files or continuous data streams.  
- Simpler to implement than asymmetric encryption.

## Disadvantages

- **Key distribution problem:** both parties must share the same secret key securely.  
- If key is compromised, all communication is exposed.  
- Not suitable for open networks without key management systems.

## Applications / Use Cases

- Encrypting data at rest (files, disks).  
- VPNs and private network communications.  
- Secure messaging systems (when key sharing is handled).  
- Database and backup encryption.

## Key Points / Notes

- The **security** of symmetric encryption depends entirely on **key secrecy**.  
- Common practice: use symmetric encryption for bulk data, and asymmetric encryption to exchange the symmetric key.  
- AES is the current **industry standard** for strong symmetric encryption.  
- Block ciphers (AES, DES) work on fixed-size blocks; stream ciphers (RC4, ChaCha20) encrypt bit-by-bit or byte-by-byte.  
