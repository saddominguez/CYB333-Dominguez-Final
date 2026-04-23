# CYB333 - Password Strength Analyzer

## Overview
This project is a Python-based Password Strength Analyzer. It evaluates passwords using security best practices and common attack patterns, then provides feedback to help users create stronger passwords.

## Features
- Checks minimum length (12+ characters)
- Requires:
  - Uppercase and lowercase letters
  - At least one number
  - At least one special character
- Detects common weak patterns (e.g., "password", "123")
- Prevents repeated characters (3 or more in a row)
- Provides:
  - Strength score (0–100)
  - Rating (Weak, Moderate, Strong)
  - Suggestions for improvement
- Hides password input for security
- Loops until a valid password is entered

## Libraries Used
- `re` – Used for pattern matching
- `getpass` – Hides password input

## How It Works
1. Displays password requirements  
2. Prompts user to enter a password (hidden input)  
3. Evaluates password strength and security  
4. Provides feedback and suggestions  
5. Repeats until a valid password is entered  

## How to Run
1. Make sure Python 3 is installed  
2. Download the file  
3. Run in terminal:

```bash
python Password.py
