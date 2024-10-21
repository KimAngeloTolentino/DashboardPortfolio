<template>
    <footer class="footer">
      <div class="container">
        <span>© 2024 Toletino's Portfolio. All Rights Reserved.</span>
      </div>
    </footer>
  </template>
  
  <script>
  export default {
    name: "AppFooter",
  };
  </script>
  
  <style scoped>
  .footer {
    background-color: #ff9800; /* Green background */
    color: #ffffff; /* White text */
    height: 60px;
    display: flex;
    align-items: center;
    justify-content: center;
    position: fixed;
    bottom: 0;
    width: 100%;
    padding: 0 20px;
    box-shadow: 0 -1px 5px rgba(0, 0, 0, 0.1); /* Subtle shadow for depth */
  }
  
  .container {
    text-align: center; /* Center text */
    font-size: 14px; /* Adjust font size */
  }
  </style>
  