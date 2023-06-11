<!DOCTYPE html>
<html>
<head>
    <title>Guess the Number</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
        }
    </style>
</head>
<body>
    <h1>Guess the Number</h1>
    <p>Try to guess the randomly generated number between 1 and 100.</p>
    <input type="text" id="guessInput" placeholder="Enter your guess">
    <button onclick="checkGuess()">Submit</button>
    <p id="message"></p>

    <script>
        // Generate a random number between 1 and 100
        const randomNumber = Math.floor(Math.random() * 100) + 1;
        let attempts = 0;

        function checkGuess() {
            const guessInput = document.getElementById("guessInput");
            const guess = parseInt(guessInput.value);
            const message = document.getElementById("message");

            if (isNaN(guess) || guess < 1 || guess > 100) {
                message.textContent = "Please enter a valid number between 1 and 100.";
            } else {
                attempts++;

                if (guess === randomNumber) {
                    message.textContent = `Congratulations! You guessed the number in ${attempts} attempt(s).`;
                    guessInput.disabled = true;
                } else if (guess < randomNumber) {
                    message.textContent = "Too low. Guess higher!";
                } else {
                    message.textContent = "Too high. Guess lower!";
                }
            }

            guessInput.value = "";
            guessInput.focus();
        }
    </script>
</body>
</html>
