
<template>
    <div class="creative-page">
      <h1>Number Guessing Game</h1>
      <p>Guess the number between 1 and 100!</p>
      <input
        type="number"
        v-model="userGuess"
        placeholder="Enter your guess"
        class="guess-input"
      />
      <button @click="checkGuess" class="guess-button">Guess</button>
      <p v-if="message" class="message">{{ message }}</p>
      <button v-if="gameOver" @click="restartGame" class="restart-button">Play Again</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'CreativePage',
    data() {
      return {
        randomNumber: Math.floor(Math.random() * 100) + 1,
        userGuess: null,
        message: '',
        gameOver: false,
      };
    },
    methods: {
      checkGuess() {
        if (this.userGuess < 1 || this.userGuess > 100) {
          this.message = 'Please enter a number between 1 and 100.';
          return;
        }
        
        if (this.userGuess < this.randomNumber) {
          this.message = 'Too low! Try again.';
        } else if (this.userGuess > this.randomNumber) {
          this.message = 'Too high! Try again.';
        } else {
          this.message = 'Congratulations! You guessed it!';
          this.gameOver = true;
        }
      },
      restartGame() {
        this.randomNumber = Math.floor(Math.random() * 100) + 1;
        this.userGuess = null;
        this.message = '';
        this.gameOver = false;
      },
    },
  };
  </script>
  
  <style scoped>
  .creative-page {
    max-width: 400px;
    margin: 50px auto;
    text-align: center;
  }
  
  .guess-input {
    padding: 10px;
    width: 80%;
    margin-bottom: 10px;
    border: 1px solid #ddd;
    border-radius: 5px;
  }
  
  .guess-button,
  .restart-button {
    padding: 10px 15px;
    background-color: #ff9800;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  
  .guess-button:hover,
  .restart-button:hover {
    background-color: #555;
  }
  
  .message {
    margin-top: 15px;
    color: #333;
  }
  </style>
  