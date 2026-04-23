# CYB333-Dominguez-Final
Password Strength Analyzer

## Overview
This project is a Password Strength Analyzer built in Python. The program evaluates the strength of a user’s password based on common security standards and known attack patterns. It also provides feedback and suggestions to help users create stronger, more secure passwords.

## Features
- **Password Strength Scoring**: Evaluates passwords on a scale of 0-100
- **Strength Classification**: Categorizes passwords as Weak, Moderate, or Strong
- **Security Validation**: Checks for:
  - Minimum 12 characters
  - At least one uppercase letter
  - At least one lowercase letter
  - At least one number
  - At least one special character (!@#$%^&*()-_=+)
  - Avoids common weak patterns (password, 123, qwerty, admin, letmein)
  - Prevents repeating characters (2+ times)
- ** Suggestions**: Provides specific recommendations for improving weak passwords
- **User-Friendly Loop**: Allows users to retry until a valid password is created
- **Secure Input**: Hides password input using  getpass 

## Dependencies and Prerequisites

### System Requirements
- **Operating System**: Windows, macOS, or Linux
- **Python Version**: Python 3.6 or higher
- **RAM**: Minimal (< 50 MB)
- **Disk Space**: < 1 MB

### Python Libraries
All required libraries are part of Python's Standard Library:
- `re` - Regular expressions module for pattern matching
- `getpass` - Secure password input module (hides input from terminal display)

### Installation Instructions

#### Step 1: Verify Python Installation
Check if Python is installed on your system:
```bash
python --version
```
or
```bash
python3 --version
```

If Python is not installed, download it from [python.org](https://www.python.org/downloads/)

#### Step 2: Download the Program
1. Clone or download the `Password.py` file to your local machine
2. Navigate to the directory containing `Password.py` in your terminal/command prompt

#### Step 3: Verify File Location
Ensure `Password.py` is in your working directory:
```bash
# On Windows
dir Password.py

# On macOS/Linux
ls Password.py
```

## How to Set Up and Run

### Option 1: Command Line (Recommended)

#### Windows PowerShell/CMD
```bash
# Navigate to the project directory
cd "path\to\Python Codes"

# Run the program
python Password.py
```

#### macOS/Linux Terminal
```bash
# Navigate to the project directory
cd path/to/Python\ Codes

# Run the program
python3 Password.py
```

### Option 2: Direct Execution
If Python is in your system PATH, you can double-click `Password.py` directly (on Windows with Python properly configured).

### Program Execution Flow

1. **Display Requirements**: Program shows password security requirements
2. **Password Input**: User enters a password (input is hidden from display)
3. **Analysis**: Program evaluates password against all criteria
4. **Display Results**: Shows:
   - Strength score (0-100)
   - Strength level classification
   - Specific suggestions for improvement
5. **Validation Check**:
   - **If Valid (score ≥ 50)**: Program accepts password and exits
   - **If Invalid (score < 50)**: User is prompted to try again with suggestions

### Example Output
```
Password Strength
------------------------------
Password Requirements:
- 12 characters minimum
- One uppercase letter required
- One lowercase letter required
- One number required
- One special character required
- Should not contain common words (ex: password, 123)
--------------------------

Enter password: 

Score: 75/100
Strength: Moderate

Suggestions:
- Do not repeat the same character multiple times.

------------------------------
Try again
```

## Scoring Breakdown
- **Length (≥12 characters)**: +25 points
- **Uppercase letter**: +15 points
- **Lowercase letter**: +15 points
- **Number**: +15 points
- **Special character**: +15 points
- **Repeating characters (3+)**: -10 points

**Validity Threshold**: Minimum score of 50 required

## Strength Levels
- **Strong**: Score ≥ 80
- **Moderate**: Score 50-79
- **Weak**: Score < 50	

## Additional Information

### Password Security Tips
- Use passphrases (multiple random words) for easier memorization
- Avoid personal information (birthdays, names, addresses)
- Never reuse passwords across different accounts
- Use unique passwords for important accounts (email, banking, etc.)
- Consider using a password manager for storing complex passwords
- Change passwords regularly for critical accounts

### How the Scoring Algorithm Works
The algorithm evaluates five key security factors:
1. **Length**: Ensures minimum 12-character requirement
2. **Character Variety**: Checks for mix of uppercase, lowercase, numbers, and special characters
3. **Weak Pattern Detection**: Blocks common passwords and patterns
4. **Character Repetition**: Penalizes excessive repetition
5. **Overall Strength**: Calculates composite score from all factors

### Code Structure
- `password_requirements()` - Displays security requirements to user
- `password_strength(password)` - Analyzes password and returns validation results
- `main()` - Orchestrates user interaction and program flow with retry loop
