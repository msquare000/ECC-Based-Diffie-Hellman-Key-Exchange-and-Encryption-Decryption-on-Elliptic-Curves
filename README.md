# ECC-Based-Diffie-Hellman-Key-Exchange-and-Encryption-Decryption-on-Elliptic-Curves
# Overview
This repository contains Python scripts implementing Elliptic Curve Cryptography (ECC) for Diffie-Hellman key exchange and encryption/decryption using elliptic curves. The ECC-based Diffie-Hellman key exchange allows two parties to securely agree upon a shared secret over an insecure channel. The elliptic curve encryption and decryption operations are demonstrated using a specific elliptic curve defined by the user's input parameters.

# Requirements
Python 3.x
SymPy library (pip install sympy) for prime number verification
# Components
## ecc_diffie_hellman.py:
This script implements ECC-based Diffie-Hellman key exchange using a specified elliptic curve.
### It includes functions for:
Verifying if an elliptic curve is valid.
Checking if a point belongs to the specified curve.
Scalar multiplication on elliptic curves using the double-and-add algorithm.
Point addition and scalar multiplication for generating public keys and shared secrets.
## elliptic_curve_encryption.py:
This script demonstrates encryption and decryption operations using elliptic curve mathematics.
### It includes functions for:
Modular inverse calculation.
Point addition and doubling on elliptic curves.
Scalar multiplication for encryption and decryption.
# Usage
## ECC-Based Diffie-Hellman Key Exchange:
Run ecc_diffie_hellman.py.
Input parameters for the elliptic curve (a, b, p) and the generator point (G).
Input private keys for each party.
The script will compute and print the shared secret.
## Elliptic Curve Encryption and Decryption:
Run elliptic_curve_encryption.py.
Provide input parameters for the elliptic curve (q, a, b) and the generator point (G).
Input the private key (nB) for encryption.
Enter coordinates for the message point (Pm).
Specify a random integer k for encryption.
The script will compute the ciphertext (Cm) and decrypt it to obtain the plaintext.
### Example
Here's a quick example of how to use these scripts:

## ECC-Based Diffie-Hellman Key Exchange:

Enter value for a: 0
Enter value for b: -4
Enter value for p (a prime number): 211
Elliptic curve is valid

Enter coordinates for the generator point (G)
Enter x coordinate of G: 2
Enter y coordinate of G: 2

[Emaan]: Enter your private key: 2
[Emaan]: Generated Public Key (to be sent to Maheen): (5, 200)

[Maheen]: Enter your private key: 1
[Maheen]: Generated Public Key (to be sent to Emaan): (2, 2)

Emaan computed Shared Secret: (5, 200)
Maheen computed Shared Secret: (5, 200)
Shared Secret Matched!
## Elliptic Curve Encryption and Decryption:

-> Enter the prime modulus (q): 257
-> Enter the coefficient 'a' of the elliptic curve: 0
-> Enter the coefficient 'b' of the elliptic curve: -4
-> Enter the x-coordinate of the base point G: 2
-> Enter the y-coordinate of the base point G: 2
-> Enter private key (nB): 101
-> Enter the x-coordinate of the message point Pm: 112
-> Enter the y-coordinate of the message point Pm: 26
-> Enter the random integer k: 41

=> Ciphertext Cm = ((136, 128), (246, 174))

=> Decrypted plaintext = (112, 26)
### Notes
The scripts utilize ANSI escape codes for colorful terminal output, which may not work on all terminals.
Ensure that the input parameters for the elliptic curve and points (G, Pm) are valid and lie on the specified curve.
