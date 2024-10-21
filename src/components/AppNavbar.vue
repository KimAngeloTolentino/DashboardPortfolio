<template>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark px-4">
      <router-link class="navbar-brand" to="/">Visionary Dashboard</router-link>
  
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
  
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav me-auto">
          <li class="nav-item">
            <router-link class="nav-link" to="/dashboard/home">Home</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" to="/dashboard/profile">Profile</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" to="/dashboard/showcase">Showcase</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" to="/dashboard/contact">Contact</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" to="/dashboard/creative">Creative</router-link>
          </li>
        </ul>
      </div>
    </nav>
  </template>
  
  <script>
  export default {
    name: "AppNavbar",
  };
  </script>
  