
<template>
    <div class="showcase">
      <h1>Portfolio</h1>
      <div class="projects">
        <div class="project-card" v-for="project in projects" :key="project.id">
          <img :src="project.image" alt="Project" class="project-image" />
          <h2>{{ project.title }}</h2>
          <p>{{ project.description }}</p>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        projects: [
          { 
            id: 1, 
            title: 'Website', 
            description: 'A personal portfolio website built with Vue.js', 
            image: require('@/assets/project1.jpg') // Ensure this image is in the assets folder
          },
          { 
            id: 2, 
            title: 'E-commerce Site', 
            description: 'A fully functional e-commerce site with Vue and Firebase', 
            image: require('@/assets/project2.jpg') // Ensure this image is in the assets folder
          },
          { 
            id: 3, 
            title: 'Social Media App', 
            description: 'A simple social media app prototype', 
            image: require('@/assets/project3.jpg') // Ensure this image is in the assets folder
          },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .showcase {
    padding: 20px;
    text-align: center;
  }
  
  .projects {
    display: flex;
    flex-wrap: wrap;
    justify-content: center; /* Center align the project cards */
  }
  
  .project-card {
    border: 1px solid #ddd;
    padding: 15px;
    margin: 10px;
    border-radius: 8px;
    text-align: center;
    width: 300px; /* Set a fixed width for cards */
    transition: box-shadow 0.3s; /* Add a transition for hover effect */
  }
  
  .project-card:hover {
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* Shadow on hover */
  }
  
  .project-image {
    width: 100%;
    height: 200px;
    object-fit: cover;
    border-radius: 8px; /* Round corners of images */
  }
  
  .project-card h2 {
    margin-top: 10px;
    font-size: 1.5em; /* Increase font size for title */
  }
  
  .project-card p {
    color: #555; /* Subtle color for description */
  }
  </style>
  