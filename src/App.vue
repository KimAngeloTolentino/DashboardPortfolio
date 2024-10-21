<template>
  <div id="app">
    <AppNavbar />
    <router-view></router-view> <!-- This will render the child components of DashboardLayout -->
    <AppFooter />
  </div>
</template>

<script>
import AppNavbar from "./components/AppNavbar.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  name: 'App',
  components: {
    AppNavbar,
    AppFooter,
  },
};
</script>

<style>
#app {
  background-color: #f8f9fa; /* Optional: Light background for the app */
  min-height: 100vh; /* Ensure full height */
  padding-bottom: 60px; /* Add space for the footer */
}
</style>
