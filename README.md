# Binary Flip Cipher

The Binary Flip Cipher is a lightweight cryptographic system created for educational purposes, showcasing fundamental encryption techniques. This project transforms text by flipping bits in binary representation, allowing students to explore bitwise operations and basic cryptography.

## 🔑 How It Works

The encryption and decryption process consists of four simple steps:

1. Convert to ASCII: Each character in the plaintext is converted to its ASCII code, representing the character as a decimal number.
2. ASCII to Binary: The ASCII code is then transformed into an 8-bit binary value, providing a basis for bit manipulation.
3. Bit-Flipping (One’s Complement): Each bit in the binary string is flipped — 0s become 1s, and 1s become 0s — creating a new binary value.
4. Binary to Decimal, then Character: The flipped binary value is converted back to decimal, then mapped to a character, resulting in the encrypted message.

The decryption process simply reverses these steps to recover the original plaintext.

## 🧩 Example

Encrypting the plaintext "hello":
- Each character goes through ASCII conversion, binary transformation, bit-flipping, and remapping to yield an encrypted output, such as "wzssp".

## ⚖️ Strengths and Limitations

- Strengths: 
  - Fast and straightforward encryption
  - Adds obscurity through bit manipulation

- Limitations: 
  - Vulnerable to frequency analysis and brute-force attacks
  - Limited to ASCII characters

## 🎓 Educational Purpose

This project was developed as part of a cryptography course, aiming to introduce students to the basics of encryption and bitwise operations. While it demonstrates fundamental cryptographic concepts, the Binary Flip Cipher is not intended for secure applications and should be viewed as a learning tool.

--- 
