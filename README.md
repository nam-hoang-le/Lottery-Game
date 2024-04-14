# Lottery-Game

## Overview

In this repository, I will applied Python to create a funny game, Lottery Game. 

I will create 3 version: Basic, Pro and Pro Max, which updated multiple features through the version due to the usage and addition of different structures and functions in Python. 

All the version was made in .ipynb file, with careful instructions for each functions.

You have to run all the cells in order to play the game.

The games are still missing many case handlers, you can support the games by adding new functions/ fixing bugs.

**Important note:** The game is just for entertainment, not for any other purposes.

## Outline 

1. Lottery Game Basic 
2. Lottery Game Pro 
3. Lottery Game Pro Max 

## Details

### Lottery Game Basic 

**Overview**

Lottery is a form of betting based on lottery results with a conversion rate of 1:70 (winning 1 receives 70). 

There are 7 prizes from First Prize to Seventh Prize every day. A player is considered to win the lottery when their chosen lottery number matches the drawn numbers. 

If they win, the prize money will be the bet amount multiplied by 70; if they lose, the bet amount will be lost. Each time a player enters the game, they will have 1,000,000 [your money rate] in hand. 

The game will have the following main functions:
- Play lottery: Users bet on a 2-digit number, then the system randomly draws 7 prizes and displays them on the screen (the lottery numbers and random draws are 2-digit numbers from 10-99).
  - If the player wins the lottery, the winning lottery number, prize money, and total amount will be displayed.
  - If the player loses the lottery, the lost lottery number and remaining money will be displayed.
  - Players will be given the option to continue playing or return to the main screen.
  - If the player runs out of money, the system will display a bankruptcy message and they will not be allowed to play anymore.
- Deposit money: Players will be allowed to deposit money to play the lottery. They can return to the main screen to select other functions.
- Exit game: Players selecting this function will exit the game.


### Lottery Game Pro 

**Overview**

This game is an updated version of Lottery Game Basic with 3 main functions: 
- Implement login functionality:
    - Upon running the program, the login screen will be displayed first. Only if the user enters the correct username and password will they be allowed to access the main screen (default username and password are admin - admin).
    - If the user enters the wrong password, prompt for re-entry. The user only needs to log in once until they log out, at which point they must log in again.
- Lottery playing feature:
    - Allow users to input multiple lottery numbers, with each number separated by a comma (e.g., 12,23).
    - The drawn numbers will consist of a total of 5 digits and may include the digit 0 at the beginning.
    - The drawn numbers will be passed into a Dictionary with the Key being the name of the prize and the Value being the drawn number. The winning conditions remain the same, but the total amount at this point will be = bet amount * (number of winning lottery numbers * 70) - bet amount for losing lottery numbers. You also need to print out which lottery numbers are winning numbers.
- Logout functionality:
    - Change the Exit function to a Logout function. After logging out, if the user wants to play the game again, they will have to log in again from the beginning.
- Note: 
    - The default username and password are "admin"

### Lottery Game Pro Max

**Overview**

This game is an upgraded version of th the Lottery Game Pro. It will have these following functions:

- Login function:
    - If it is an admin account, there will be a separate menu consisting of account management, account deposit, statistics, and logout.
    - If it is a regular account, the regular menu will be displayed including: play lottery, change password, statistics, and logout.
- Admin function:
    - Account management: Create accounts (not allowed to create duplicate usernames) and delete accounts (not allowed to delete admin accounts). Account information includes username, password, total money, and is saved in the taikhoan.txt file, with each account on one line.
    - Deposit money: The deposit function will update the account balance in the taikhoan.txt file.
    - Statistics: The statistics function will count the number of accounts, the number of lottery plays, and the win/loss ratio.
- User function:
    - Change password function: Players can change their passwords.
    - Play lottery function: Each time a lottery is played, the information will be automatically saved to the choilo.txt file, including: play time, username, lottery number bet, bet amount, draw result, lottery win result, each play on one line.
    - Statistics function: Allows users to view statistics such as the number of times they played the lottery, total winnings from lottery plays, total losses from lottery plays, win/loss ratio.

- Module construction: Transfer all the functions above into one module called LoDeHoc. Build a File Processing Module with the input as the file path and the output as a list of data read from the file. Both modules are located in the my_lib directory.