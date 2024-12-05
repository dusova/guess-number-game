# Number Guessing Game

This project is a simple web-based game where users try to guess a randomly selected number between 1 and 100.

## Features

- A random number between 1 and 100 is generated.
- The user enters a number in an input field and clicks the "Guess" button to make a guess.
- "Higher" or "Lower" messages are displayed until the user guesses the correct number.
- When the correct guess is made, the number of attempts is displayed.

## Usage

1. Download the project and run it on a local server or in your browser.
2. Open the page and start guessing a number between 1 and 100.
3. Enter the number and click the "Guess" button.
4. Follow the hint messages to find the correct number.

## Files

- `index.html`: The main HTML file where the game is located.
- `script.js`: The game logic written in JavaScript (if you want to use an external script file).

## How It Works

- A random number between 1 and 100 is generated using the `Math.random()` function.
- When the user makes a guess, the number is checked.
    - If the guessed number is correct, a success message is displayed.
    - If the guessed number is too high, a "Guess a lower number" message is displayed.
    - If the guessed number is too low, a "Guess a higher number" message is displayed.

## Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Number Guessing Game</title>
</head>
<body>
        <h1>Number Guessing Game</h1>
        <p>Guess a number between 1 and 100!</p>
        <input type="number" id="guessInput" placeholder="Enter your guess">
        <button onclick="checkGuess()">Guess</button>
        <p id="message"></p>

        <script>
                const randomNumber = Math.floor(Math.random() * 100) + 1;
                let attempts = 0;

                function checkGuess() {
                        const userGuess = document.getElementById("guessInput").value;
                        attempts++;
                        if (userGuess == randomNumber) {
                                document.getElementById("message").innerText = `Congratulations! You guessed the correct number in ${attempts} attempts.`;
                        } else if (userGuess > randomNumber) {
                                document.getElementById("message").innerText = "Guess a lower number.";
                        } else {
                                document.getElementById("message").innerText = "Guess a higher number.";
                        }
                }
        </script>
</body>
</html>
```

## Contributing

If you would like to contribute to this project, please send a pull request or open an issue. We welcome all feedback!

## License

This project is licensed under the [MIT License](LICENSE).
