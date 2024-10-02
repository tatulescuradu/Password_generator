# Password Generator

This project is a Python script that generates secure passwords based on user-defined constraints, such as the number of digits, special characters, uppercase, and lowercase letters. The script uses Python's `secrets` module for cryptographic randomness, ensuring that the passwords are strong and secure.

## Function: `generate_password`

### Description
The `generate_password` function generates a random password that meets specific requirements such as:
- Length of the password.
- Minimum number of digits.
- Minimum number of special characters.
- Minimum number of uppercase letters.
- Minimum number of lowercase letters.

### Parameters
- `length` (int): Length of the password to be generated. Default is 16.
- `nums` (int): Minimum number of digits required in the password. Default is 1.
- `special_chars` (int): Minimum number of special characters required. Default is 1.
- `uppercase` (int): Minimum number of uppercase letters required. Default is 1.
- `lowercase` (int): Minimum number of lowercase letters required. Default is 1.

### Returns
- A randomly generated password as a string that fulfills the given constraints.

### Example Usage

```python
# Default usage with default parameters
new_password = generate_password()
print('Generated password:', new_password)
# Output: Generated password: gZ8k%R#9wHx2Y!a1

# Custom usage with specific parameters
custom_password = generate_password(length=20, nums=3, special_chars=2, uppercase=4, lowercase=3)
print('Generated password:', custom_password)
# Output: Generated password: A#JkL3!g2H1z9Df&RtP4
```

### How It Works
1. The function defines a pool of characters to choose from, including uppercase and lowercase letters, digits, and special symbols.
2. It uses the `secrets.choice()` method from Python's `secrets` module to generate a random password of the specified length.
3. The function ensures that the password meets all the provided constraints (e.g., minimum number of digits, special characters, etc.) using regular expressions (`re.findall()`).
4. If the generated password does not meet the constraints, the function generates a new one until it does.

### How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/password-generator.git
   cd password-generator
   ```
2. Install any required dependencies (if applicable).
3. Run the script in a Python 3.x environment:
   ```bash
   python generate_password.py
   ```

### Acknowledgments
This project was created with the help of Python programming courses from [FreeCodeCamp.org](https://www.freecodecamp.org/), which provided foundational knowledge in Python programming, cryptographic security, and regular expressions.
