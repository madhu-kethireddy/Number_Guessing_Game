# Number Guessing Game

Welcome to the Number Guessing Game! This interactive game challenges users to guess a randomly generated number between 1 and 1000. The game also tracks user statistics, including the number of games played and the best game (fewest guesses).

## Getting Started

### Prerequisites

- Bash shell
- PostgreSQL

### Installation

1. Clone the repository:
    ```bash
    git clone <repository_url>
    cd number_guessing_game
    ```

2. Make the script executable:
    ```bash
    chmod +x number_guess.sh
    ```

3. Create the database:
    ```bash
    psql --username=freecodecamp --dbname=postgres -c "CREATE DATABASE number_guess;"
    ```

4. Set up the database tables:
    ```bash
    psql --username=freecodecamp --dbname=number_guess -f create_tables.sql
    ```

### Running the Game

To start the game, execute the script:
```bash
./number_guess.sh
```

### How to Play

1. Enter your username when prompted.
2. If you are a returning user, your game statistics will be displayed.
3. Guess the secret number between 1 and 1000.
4. The script will provide hints if your guess is too high or too low.
5. Continue guessing until you find the secret number.
6. Your game statistics will be updated and displayed.

### Database Backup

1. To save your database progress, create a dump:
   ```sql
   pg_dump -cC --inserts -U freecodecamp number_guess > number_guess.sql

2. To restore the database from the dump:
   ```sql
   psql -U postgres < number_guess.sql

### Git Commit Messages

- Initial commit
- fix: Resolved database connection issue
- feat: Implemented user statistics tracking
- refactor: Enhanced input validation
- chore: Updated README.md

### Contributing

Contributions are welcome! Feel free to fork this repository and submit pull requests. For major changes, please open an issue first to discuss your ideas.

### License

This project is licensed under the MIT License.

I hope this version suits your needs! If you need any more adjustments or have other questions, feel free to ask.
