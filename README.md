# Roman-Emperor-s-Cipher-Solver

This Python script is designed to help you decrypt a cipher text using a shift-based substitution cipher (a variant of the Caesar cipher). The program tries all 26 possible keys, letting you see the output for each one so that you can choose the correct decryption.

## Overview

- **Functionality:**  
  The script defines a function `poly(plain: str, key: int) -> str` which:
  - Converts the input text to lowercase.
  - Constructs a substitution dictionary by shifting the alphabet by the given key.
  - Encrypts/decrypts the text using this dictionary and returns the result in uppercase.

- **Usage:**  
  The program iterates through all possible shift keys (0 to 25) and prompts the user to input a cipher text for each iteration. It then displays the decrypted output along with the corresponding key number.

## Requirements

- **Python Version:** Python 3.x  
- **Libraries:** Uses only Python's standard library (specifically, the `string` module).

## How It Works

1. **Substitution Dictionary:**  
   The `poly` function builds a dictionary mapping each letter of the alphabet to another letter shifted by a specific key. For example, if the key is `1`, then:
   - `'z'` maps to `'a'`
   - `'a'` maps to `'b'`
   - `'b'` maps to `'c'`
   - ... and so on.

2. **Encryption/Decryption:**  
   The inner function `encdec` uses this dictionary to translate each character in the input text. Non-alphabet characters are left unchanged.

3. **Key Iteration:**  
   The main loop of the script runs the decryption function for all 26 keys. It prints the resulting text for each key so you can inspect the output and find the correctly decrypted message.

## Installation and Running

1. **Download the Code:**
   - Save the provided code into a file named `solve.py`.

2. **Run the Script:**
   - Open a terminal (or command prompt).
   - Navigate to the directory containing `solve.py`:
     ```bash
     cd /path/to/your/directory
     ```
   - Run the script using:
     ```bash
     python3 solve.py
     ```
     *(If your system uses `python` instead of `python3`, adjust accordingly.)*

3. **Interacting with the Program:**
   - The script will display the prompt:
     ```
     UMHTGSJV TWXGJW DGSV TJAUC
     ```
   - Enter the cipher text (for example, press Enter to use the default text if it matches your intended input).
   - The program will then print the decrypted results for each key.

## Example Output

For the cipher text:
```
UMHTGSJV TWXGJW DGSV TJAUC
```
the script will output 26 lines like:
```
[DECRYPTED TEXT], Key: 1
[DECRYPTED TEXT], Key: 2
...
[DECRYPTED TEXT], Key: 26
```
Review the output to determine which key produces a meaningful message.

## Customization

If you want to bypass manual input every time, replace the line:
```python
cipher_input = input("Enter the string to be deciphered")
```
with:
```python
cipher_input = "Enter the string to be deciphered"
```
This modification will automatically use the specified cipher text for every iteration.

## License

This code is provided "as-is" without any warranty. Feel free to use, modify, and distribute it according to your needs.

## Author

*Edoscoba*
