# Cryptography Practical (OpenSSL)

## Objective
Demonstrate symmetric encryption and decryption of a file using OpenSSL's AES-256-CBC cipher.

---

## Step 1: Create a Sample File

```bash
echo "Hello ApexPlanet" > message.txt
```

## Step 2: Encrypt the File

```bash
openssl enc -aes-256-cbc -salt -in message.txt -out message.enc
```
This encrypts `message.txt` using the AES-256-CBC algorithm with a salted key derived from a passphrase, producing `message.enc`.

## Step 3: Decrypt the File

```bash
openssl enc -aes-256-cbc -d -in message.enc -out decrypted.txt
```
The `-d` flag reverses the process, decrypting `message.enc` back into readable text using the same passphrase.

## Step 4: Verify

```bash
cat decrypted.txt
```
Confirms that the decrypted content matches the original file exactly.

---

## Key Concepts

- **Symmetric Encryption**: Same key is used for both encryption and decryption (as opposed to asymmetric encryption, which uses a public/private key pair).
- **AES-256**: A widely trusted symmetric block cipher using a 256-bit key, considered secure for most modern applications.
- **CBC (Cipher Block Chaining)**: Each block of plaintext is XORed with the previous ciphertext block before encryption, ensuring identical plaintext blocks do not produce identical ciphertext.
- **Salting**: Adds random data to the key derivation process to prevent precomputed dictionary attacks (e.g., rainbow tables).

---

## Relevance to Security

Encryption underpins the **Confidentiality** principle of the CIA Triad. Understanding how to encrypt and decrypt data manually helps in recognizing how secure communication channels, password storage, and file protection mechanisms work in real-world systems.
