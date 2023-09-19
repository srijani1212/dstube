<template>
  <div>
    <div v-if="showProfile" class="profile-form">
      <!-- Input fields for First Name, Last Name, Mobile Number, Email -->
      <input v-model="firstName" placeholder="First Name" class="input-field" />
      <input v-model="lastName" placeholder="Last Name" class="input-field" />
      <input v-model="mobileNumber" placeholder="Mobile Number" class="input-field" />
      <input v-model="email" placeholder="Email" class="input-field" />
      <button @click="updateProfile" class="update-button">Update</button>
    </div>
    <div v-if="detailsVisible" class="profile-details">
      <!-- Display profile details -->
      <p>Name: {{ fullName }}</p>
      <p>Mobile Number: {{ mobileNumber }}</p>
      <p>Email: {{ email }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      firstName: "",
      lastName: "",
      mobileNumber: "",
      email: "",
      showProfile: true, // Initially, show the profile input form
      detailsVisible: false,
    };
  },
  computed: {
    fullName() {
      return `${this.firstName} ${this.lastName}`;
    },
  },
  methods: {
    updateProfile() {
      // Show profile details after clicking the Update button if any of the fields are filled
      if (this.firstName || this.lastName || this.mobileNumber || this.email) {
        this.detailsVisible = true;
        this.showProfile = false; // Hide the input form
      }
    },
  },
};
</script>

<style scoped>
/* Your existing styles remain unchanged */
</style>
