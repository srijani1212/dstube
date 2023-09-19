<template>
  <div class="header-container">
    <div class="button-container">
      <Button buttonClass="ds-tube-button">DsTube</Button> <!-- DsTube button -->
    </div>
    <div class="search-bar">
      <TextField /> <!-- Import and use the TextField component for the search bar -->
    </div>
    <div class="button-container">
      <Button buttonClass="profile-button">Profile</Button> <!-- Profile button -->
    </div>
  </div>
</template>

<script>
import Button from './Button.vue'; // Import the Button component
import TextField from './TextField.vue'; // Import the TextField component

export default {
  components: {
    Button,
    TextField,
  },
};
</script>

<style scoped>
.header-container {
  width: 100%;
  height: 125px;
  background: #202020;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 100;
  padding: 10px 20px; /* Add padding for spacing */
}

.button-container {
  display: flex;
  align-items: center;
  margin-left:20px;
  margin-right:40px;
}

.search-bar {
  flex-grow: 1; /* Allow the search bar to take remaining space */
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
}

/* You can add more specific styles for your Button and TextField components here */
</style>
