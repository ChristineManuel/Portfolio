<template>
    <div class="dashboard">
      <header class="header-topbar">
        <h1 class="title">⋅˚₊‧ ୨ Christine's Portfolio ୧ ‧₊˚ ⋅</h1>
        <nav class="topbar">
          <ul>
            <li><router-link to="/dashboard/profile">Profile</router-link></li>
            <li><router-link to="/dashboard/portfolio">My Works</router-link></li>
            <li><router-link to="/dashboard/contact">Contact</router-link></li>
            <li><router-link to="/dashboard/creative">Be creative with me!</router-link></li>
            <li class="logout"><button @click="logout">Logout</button></li> <!-- Logout button -->
          </ul>
        </nav>
      </header>
      <main class="content">
        <router-view />
      </main>
    </div>
  </template>
  
  
  <script>
  export default {
    name: 'DashboardPage',
    methods: {
      logout() {
        // Implement logout logic
        // clear user data and redirect to login page
        console.log('User logged out'); // Replace with actual logout logic
        this.$router.push('/'); // Redirect to login page
      },
    },
  };
  </script>
  
  
  <style scoped>
  .dashboard {
    display: flex;
    flex-direction: column;
    font-family: Arial, sans-serif;
  }
  
  .header-topbar {
    display: flex;
    flex-direction: column;
    background: rgba(255, 255, 255, 0.8); /* Semi-transparent background */
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 1000;
  }
  
  .title {
    color: #2b094a;
    font-size: 2rem;
    margin: 20px 0;
    text-align: center;
  }
  
  .topbar {
    background: rgba(120, 71, 122, 0.8); /* Semi-transparent background */
    color: white;
    padding: 10px;
  }
  
  .topbar ul {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    justify-content: space-between; /* Adjust to space items evenly */
    align-items: center; /* Center items vertically */
  }
  
  .topbar ul li {
    margin-bottom: 0;
  }
  
  .topbar ul li a {
    color: white;
    text-decoration: none;
    padding: 8px 12px;
    border-radius: 4px;
    transition: background 0.3s ease;
  }
  
  .topbar ul li a:hover {
    background: rgba(255, 255, 255, 0.576); /* Slightly darker on hover */
  }
  
  .logout {
    margin-left: auto; /* Push the logout button to the right */
  }
  
  .logout button {
    background-color: #ffffff; /* Red background for the logout button */
    color: #2b094a;
    border: none;
    padding: 8px 12px;
    border-radius: 4px;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  
  .logout button:hover {
    background-color: #2b094a75; /* Darker red on hover */
  }
  
  .content {
    padding: 20px;
    flex: 1;
    margin-top: 160px; /* Ensure content is below the fixed header */
    background: url('/src/assets/BackGround.png') no-repeat center center fixed; /* Direct link to a GIF */
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  }
  
  @media (max-width: 768px) {
    .topbar ul {
      flex-direction: column;
      align-items: center;
    }
  
    .topbar ul li {
      margin: 5px 0;
    }
  }
  </style>
  