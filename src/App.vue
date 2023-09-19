<!-- App.vue -->

<template>
  <div>
    <Header @profile-clicked="displayProfile" /> <!-- Include the Header component and listen for the custom event -->
    
    <!-- Add other content for the Home page below the header -->
    
    <!-- Render the Main component when isProfileVisible is false -->
    <Main v-if="!isProfileVisible" />
    
    <!-- Render the Profile component when isProfileVisible is true -->
    <Profile v-else />
  </div>
</template>

<script>
import Header from './components/Header.vue'; // Import the Header component using an alias
import Main from './components/Main.vue'; // Import the Main component using an alias
import Profile from './components/Profile.vue'; // Import the Profile component

export default {
  components: {
    Header, // Register the Header component
    Main, // Register the Main component
    Profile, // Register the Profile component
  },
  data() {
    return {
      isProfileVisible: false, // Add a data property to control the visibility of the Profile component
    };
  },
  methods: {
    displayProfile() {
      // Toggle the visibility of the Profile component when the Profile button is clicked
      //this.isProfileVisible = !this.isProfileVisible;
      this.isProfileVisible = true;

    },
  },
};
</script>

<style scoped>
/* Your existing styles remain unchanged */
</style>
