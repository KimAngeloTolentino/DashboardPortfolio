<template>
    <div class="d-flex flex-column" id="wrapper">
      <div class="content">
        <router-view></router-view> <!-- This will render the routed components -->
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'DashboardLayout',
  };
  </script>
  
  <style scoped>
  .content {
    padding: 20px; /* Adjust padding as needed */
  }
  </style>
  