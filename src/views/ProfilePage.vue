<template>
    <div class="profile-container">
      <img :src="profileImage" alt="Profile Picture" class="profile-pic" />
      <h2>{{ name }}</h2>
      <p class="profile-info">Email: {{ email }}</p>
      <p class="profile-info">Contact Number: {{ contactNumber }}</p>
      <p class="profile-info">Address: {{ address }}</p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        profileImage: require('@/assets/profile.jpg'), // Ensure this image is in the assets folder
        name: 'Kim Angelo Tolentino',
        email: 'kimangelo@example.com',
        contactNumber: '+09819989911',
        address: '123 Main St, Anytown, USA',
      };
    },
  };
  </script>
  
  <style scoped>
  .profile-container {
    max-width: 400px; /* Set max width for the profile card */
    margin: 50px auto; /* Center the profile card */
    text-align: center; /* Center align text */
    padding: 20px; /* Add padding for spacing */
    border: 1px solid #ddd; /* Light border for separation */
    border-radius: 8px; /* Rounded corners for a softer look */
    background-color: #f9f9f9; /* Light background for contrast */
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1); /* Subtle shadow for depth */
  }
  
  .profile-pic {
    width: 120px; /* Size of the profile picture */
    height: 120px; /* Size of the profile picture */
    border-radius: 50%; /* Circular profile picture */
    object-fit: cover; /* Ensure the image covers the circle */
    margin-bottom: 20px; /* Space below the image */
  }
  
  .profile-info {
    margin: 5px 0; /* Margin for each profile info line */
    color: #555; /* Subtle color for text */
    font-size: 1.1em; /* Slightly larger font size for readability */
  }
  </style>
  