<template>
    <div class="contact-page">
      <h2 class="contact-header">Let's Connect ⋆𐙚₊˚⊹♡</h2>
      <p>Reach me through the following channels!</p>
      <ul class="contact-list">
        <li>
          <i class="fa fa-envelope" aria-hidden="true"></i>
          <strong>Email:</strong>
          <a href="mailto:christinejmnl@gmail.com">christinejmnl@gmail.com</a>
        </li>
        <li>
          <i class="fa fa-linkedin" aria-hidden="true"></i>
          <strong>LinkedIn:</strong>
          <a href="https://www.linkedin.com/in/christinejmnl/" target="_blank">linkedin.com/in/christinejmnl</a>
        </li>
        <li>
          <i class="fa fa-github" aria-hidden="true"></i>
          <strong>GitHub:</strong>
          <a href="https://github.com/ChristineManuel" target="_blank">hhttps://github.com/ChristineManuel</a>
        </li>
        <li>
          <i class="fa fa-phone" aria-hidden="true"></i>
          <strong>Phone:</strong>
          <a href="tel:09662167269">09662167269</a>
        </li>
        <li>
          <i class="fa fa-home" aria-hidden="true"></i>
          <strong>Address:</strong>
          <p>Manila, Philippines</p>
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ContactPage',
  };
  </script>
  
  <style scoped>
  .contact-page {
    padding: 20px;
    background-color: rgba(255, 255, 255, 0.8); /*Maroon*/
    border-radius: 8px; /* Rounded corners */
    box-shadow: 0 0 10px rgba(25, 10, 10, 0.5); /*shadow*/
    text-align: center; /* Center-align*/
    color: #2b094a; /* Light text color*/
  }
  
  .contact-header {
    margin-bottom: 10px; /* Space below the header */
    color: #2b094a; /* header text is also light */
  }
  
  .contact-list {
    list-style-type: none; /* Remove bullet points */
    padding: 0; /* Remove padding */
    margin: 0; /* Remove margin */
    display: inline-block; /* Center the list block */
  }
  
  .contact-list li {
    margin-bottom: 15px; /* Space between list items */
    font-size: 1.1rem; /* Slightly larger text for readability */
    display: flex; /* Use flexbox for alignment */
    align-items: center; /* Center items vertically */
    justify-content: center; /* Center items horizontally */
  }
  
  .contact-list i {
    margin-right: 10px; /* Space between the icon and the text */
    font-size: 1.5rem; /* Adjust icon size */
    color: #2b094a; /* Light icon color for readability */
  }
  
  .contact-list a {
    color: #631366; /* Light blue color for links */
    text-decoration: none; /* Remove underline */
  }
  
  .contact-list a:hover {
    text-decoration: underline; /* Underline on hover */
  }
  
  .contact-list strong {
    margin-right: 10px; /* Space between the label and the link */
    color: #2b094a; /* Ensure strong text is readable */
  }
  
  p {
    color: #2b094a; /* Ensure general text is readable */
  }
  </style>
  