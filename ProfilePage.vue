<template>
    <div class="about-me">
      <h1>About Me</h1>
      <div class="profile-section">
        <div class="profile-info">
          <div class="info-group">
            <p>
              {{ biography }}
            </p>
          </div>
  
          <div class="info-group" v-if="resumeFile">
            <p>
              <strong>Here is my Resume ⸜(｡˃ ᵕ ˂ )⸝♡ </strong> 
              <a :href="resumeUrl" target="_blank">{{ resumeFile.name }}</a>
            </p>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  // Sample data for demonstration
  const biography = ref('Welcome to my corner of creativity! °ᡣ𐭩 . ° . I’m Christine, a Computer Engineering student who is passionate about bringing ideas to life through beautiful design and intuitive front-end development. I love blending my creativity with technology to display my ideas as well as to expressi myself. My goal is to create experiences that not only look great but also feel effortless for users.');
  
  const resumeFile = ref(new File(["Know more about me 𐙚"], "Manuel_CV.pdf")); // Dummy file for demonstration
  const resumeUrl = ref('/Manuel_CV.pdf'); // URL to your resume file in the public directory
  </script>
  
  <style scoped>
  .about-me {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background: none; /* Remove background color */
    padding: 50px;
    height: auto; /* Adjust height to fit content */
    color: #2b094a; /* Light text for contrast */
  }
  
  h1 {
    color: #2b094a; /* White heading for better visibility */
    margin-bottom: 20px;
    text-align: center;
    font-size: 2.5rem;
    letter-spacing: 1.5px;
  }
  
  .profile-section {
    padding: 30px;
    border-radius: 10px; /* Optional: Rounded corners */
    max-width: 800px;
    width: 100%;
    background: none; /* No background */
  }
  
  .profile-info {
    text-align: justify;
    color: #2b094a; /* Light gray for readability */
  }
  
  a {
    color: #631366; /* Light blue for links */
    text-decoration: none;
  }
  
  a:hover {
    text-decoration: underline; /* Underline on hover */
  }
  </style>
  