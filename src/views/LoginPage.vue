<template>
    <div class="login">
      <h1>Login</h1>
      <form @submit.prevent="login">
        <input v-model="username" placeholder="Username" required />
        <input type="password" v-model="password" placeholder="Password" required />
        <button type="submit">Login</button>
      </form>
      <p v-if="error" class="error">{{ error }}</p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        username: '',
        password: '',
        error: ''
      };
    },
    methods: {
      login() {
        if (this.username === 'user' && this.password === 'password') {
          this.$router.push({ name: 'Home' });
        } else {
          this.error = 'Invalid credentials, please try again.';
        }
      }
    }
  };
  </script>
  
  <style scoped>
  .login {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 40px;
    max-width: 400px;
    margin: auto;
    background-color: #fff; /* White background for contrast */
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    margin-top: 150px;
  }
  
  h1 {
    margin-bottom: 20px;
    font-family: 'Arial', sans-serif;
    color: #333;
  }
  
  input {
    width: 100%;
    padding: 12px;
    margin: 10px 0;
    border: 1px solid #ccc;
    border-radius: 4px;
    font-size: 14px;
  }
  
  input:focus {
    border-color: #ff9800; /* Focus border in orange */
    outline: none;
  }
  
  button {
    padding: 12px;
    background-color: #ff9800; /* Orange background for button */
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 16px;
    margin-left: 125px;
  }
  
  button:hover {
    background-color: #e68a00; /* Darker shade of orange on hover */
  }
  
  .error {
    color: red;
    margin-top: 10px;
  }
  </style>
  