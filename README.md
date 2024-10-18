
# Bank Management System

This is a simple console-based **Bank Management System** written in C++. The program allows users to manage bank accounts by performing operations such as creating an account, depositing or withdrawing money, checking balances, modifying account details, and deleting accounts.

## Features

- **Create a new account:** Users can open a new account by providing a unique account number, name, account type (savings or current), and an initial deposit.
- **Deposit amount:** Users can deposit money into an account by entering the account number.
- **Withdraw amount:** Users can withdraw money from an account, provided there is a sufficient balance.
- **Balance enquiry:** Users can check the balance of a specific account by providing the account number.
- **List all accounts:** Displays a list of all accounts with account number, account holder name, account type, and balance.
- **Modify account:** Users can modify the details of an existing account (name, account type, balance).
- **Close account:** Users can delete an existing account from the system.

## How to Run

1. **Compile the code**:
   Use a C++ compiler like `g++` to compile the code. Run the following command:

   ```bash
   g++ bankingsystem.cpp -o bankingsystem
   ```

2. **Run the executable**:
   After compiling, run the generated executable file:

   ```bash
   ./bankingsystem  # On Unix-based systems
   bankingsystem.exe # On Windows
   ```

3. **Follow the prompts**:
   The program will display a main menu with options to create an account, deposit, withdraw, etc. Select an option by entering the corresponding number.

## File Handling

The program uses **binary file handling** to store and manage account data persistently. The data is stored in `account.dat`. Every time a user creates, updates, or deletes an account, the file is updated accordingly.

- **account.dat:** The main data file where account details are stored.
- **Temp.dat:** A temporary file used when modifying or deleting accounts.

## Class Structure

The program is structured around the `account` class, which contains the following member functions:

### Member Functions:
- `create_account()`: Takes input for account creation.
- `show_account()`: Displays account details.
- `modify()`: Allows modification of account details.
- `dep()`: Increases the balance by a specified amount (deposit).
- `draw()`: Decreases the balance by a specified amount (withdrawal).
- `report()`: Displays account details in a formatted list (used for displaying all accounts).
- `retacno()`: Returns the account number.
- `retdeposit()`: Returns the current balance.
- `rettype()`: Returns the account type (savings or current).

### Other Functions:
- `write_account()`: Writes a new account to the file.
- `display_sp()`: Displays a specific account's details.
- `modify_account()`: Modifies an existing account.
- `delete_account()`: Deletes an existing account.
- `display_all()`: Lists all accounts.
- `deposit_withdraw()`: Handles both deposits and withdrawals.

## Sample Menu

The program displays a main menu with the following options:

```
======================
BANK MANAGEMENT SYSTEM
======================

::MAIN MENU::

1. NEW ACCOUNT
2. DEPOSIT AMOUNT
3. WITHDRAW AMOUNT
4. BALANCE ENQUIRY
5. ALL ACCOUNT HOLDER LIST
6. CLOSE AN ACCOUNT
7. MODIFY AN ACCOUNT
8. EXIT

Select Your Option (1-8):
```

## Notes

- The `system("CLS")` and `system("clear")` commands, used to clear the console screen, have been commented out for cross-platform compatibility.
- Ensure that `account.dat` is available in the same directory when running the program to store account data.
