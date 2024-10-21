<p class="card-text fs-4">12</p><template>
    <div class="container mt-4">
      <h2 class="mb-4 text-center">DASHBOARD</h2>
      <p class="text-center mb-4">
        Feel free to tweak it to better align with your vision!
      </p>
  
      <div class="row g-4">
        <div class="col-md-6 col-lg-3">
          <div class="card bg-creative shadow-sm">
            <div class="card-body">
              <h5 class="card-title">Creative</h5>
              <p class="card-text fs-4">1,245</p>
              <i class="bi bi-people card-icon"></i>
            </div>
          </div>
        </div>
  
        <div class="col-md-6 col-lg-3">
          <div class="card bg-showcase shadow-sm">
            <div class="card-body">
              <h5 class="card-title">Showcase</h5>
              <p class="card-text fs-4">32</p>
              <i class="bi bi-folder-open card-icon"></i>
            </div>
          </div>
        </div>
  
        <div class="col-md-6 col-lg-3">
          <div class="card bg-contacts shadow-sm">
            <div class="card-body">
              <h5 class="card-title">Commissions</h5>
              <p class="card-text fs-4">5</p>
              <i class="bi bi-calendar-event card-icon"></i>
            </div>
          </div>
        </div>
  
        <div class="col-md-6 col-lg-3">
        <div class="card bg-projects shadow-sm">
          <div class="card-body">
            <h5 class="card-title">Projects</h5>
            <p class="card-text fs-4">12</p>
            <i class="bi bi-list-task card-icon"></i>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'HomePage',
  };
  </script>
  
  <style scoped>
  .card {
    position: relative;
    border-radius: 10px;
    overflow: hidden;
    border: 1px solid #e0e0e0; /* Light gray border for definition */
  }
  
  .card-icon {
    position: absolute;
    top: 10px;
    right: 15px;
    font-size: 2rem;
    color: #aaa; /* Subtle gray for the icons */
    opacity: 0.5; /* Slight transparency */
  }
  
  .text-center {
    text-align: center;
  }
  
  .bg-creative {
    background-color: #ffcc80; /* Light orange */
  }
  
  .bg-showcase {
    background-color: #ffb74d; /* Medium orange */
  }
  
  .bg-contacts {
    background-color: #ff9800; /* Darker orange */
  }
  
  .bg-projects {
    background-color: #f57c00; /* Burnt orange */
  }
  
  h2 {
    color: #333; /* Dark gray for the heading */
  }
  
  .card-title {
    color: #555; /* Medium gray for card titles */
  }
  
  .card-text {
    color: #777; /* Lighter gray for text */
  }
  </style>
  