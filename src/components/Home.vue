<template>
    <div>
      <Header /> <!-- Include the Header component -->
      <!-- Add other content for the Home page below the header -->

      <Main /> <!-- Include the Main component -->

    </div>
  </template>
  
  <script>
  import Header from './Header.vue'; // Import the Header component using an alias
  import Main from './Main.vue'; // Import the Main component using an alias
  
  export default {
    components: {
      Header, // Register the Header component
      Main,
    },
  };
  </script>
