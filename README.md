# Binary Flip Cipher

The **Binary Flip Cipher** is a simple encryption-decryption system designed for educational purposes, demonstrating basic bitwise operations. This project transforms text by flipping bits in binary representation, allowing users to gain hands-on experience with fundamental cryptographic processes.

## How It Works

### Encryption Steps:
1. bitwise operations. This projec Each character in the plaintext is converted to its ASCII code.
2. ASCII to Binary: The ASCII code is then converted to an 8-bit binary string.
3. Bit-Flipping (One’s Complement): Each bit in the binary string is flipped—0s become 1s, and 1s become 0s.
4. Binary to Decimal, then Character: The flipped binary value is converted back to decimal, which is then mapped to a new character, creating the encrypted message.

The decryption process simply reverses these steps, starting from the decimal and reversing each transformation.

## Example Code

Here’s a Python-style pseudocode to illustrate the main functions of thes. This project tranclass:

```python
class BinaryFlipCipher:
    # Convert character to ASCII
    def convert_to_ascii(character):
        return ord(character)

    # Convert ASCII to 8-bit binary
    def convert_to_binary(decimal_value):
        return bin(decimal_value)[2:].zfill(8)

    # Flip the bits (one’s complement)
    def flip_bits(binary_value):
        return ''.join('1' if bit == '0' else '0' for bit in binary_value)

    # Convert binary back to decimal
    def convert_to_decimal(binary_value):
        return int(binary_value, 2)

    # Convert decimal back to character
    def convert_to_character(decimal_value):
        return chr(decimal_value)

    # Encode the plaintext message
    def encode_message(plaintext):
        encoded_message = ""
        for character in plaintext:
            ascii_value = convert_to_ascii(character)
            binary_value = convert_to_binary(ascii_value)
            flipped_binary = flip_bits(binary_value)
            decimal_value = convert_to_decimal(flipped_binary)
            encoded_message += convert_to_character(decimal_value)
        return encoded_message

    # Decode the encoded message
    def decode_message(encoded_message):
        decoded_message = ""
        for character in encoded_message:
            decimal_value = convert_to_ascii(character)
            flipped_binary = convert_to_binary(decimal_value)
            original_binary = flip_bits(flipped_binary)
            ascii_value = convert_to_decimal(original_binary)
            decoded_message += convert_to_character(ascii_value)
        return decoded_message

Example Walkthrough

Encrypting "hello":
 1. Convert each character to ASCII: h=104, e=101, l=108, o=111
 2. ASCII to binary: 104 -> 1101000, 101 -> 1100101, etc.
 3. Flip bits: 1101000 -> 0010111, 1100101 -> 0011010, etc.
 4. Convert flipped binary to decimal, then to character: w, z, s, p
Resulting ciphertext: "wzssp"

Decrypting "wzssp":
 1. Start from the decimal values of each character, reverse bit-flipping, and retrieve the ASCII values to reconstruct the original plaintext: "hello"

Strengths and Weaknesses

 • Strengths: Simple, fast, and provides a basic layer of obscurity by flipping binary bits.
 • Weaknesses: Vulnerable to frequency analysis and brute-force attacks, and limited to ASCII characters.

Project Context

This project is developed for the SEC 2213 Applied Cryptography course and serves as an educational exercise in cryptographic basics. While it introduces students to encryption concepts, the Binary Flip Cipher is not secure by modern cryptographic standards and is intended only as a learning tool.

