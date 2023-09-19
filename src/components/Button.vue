<template>
  <button :class="buttonClass">
    <slot></slot>
  </button>
</template>

<script>
export default {
  props: {
    buttonClass: String, // You can pass additional classes if needed
    marginStyle: String, // Add a prop for margin style
  },
};
</script>

<style scoped>
button {
  font-family: Roboto;
  font-size: 20px;
  font-weight: 700;
  letter-spacing: 0em;
  text-align: center;
  border: none;
  cursor: pointer;
  outline: none;
  padding: 10px 20px; /* Add padding for spacing */
  border-radius: 5px; /* Add border radius for rounded corners */
}

/* Apply specific styles using the buttonClass */
.ds-tube-button {
  background-color: #FF0000; /* Red background like the YouTube subscribe button */
  color: white; /* White text color */
  border: 2px solid #FF0000; /* Red border */
}

.profile-button {
  background-color: transparent; /* Transparent background */
  color: #3EA6FF; /* Blue text color */
  border: 2px solid #3EA6FF; /* Blue border */
}

/* Apply margin style if provided */
.with-margin {
  margin-right: 20px; /* Adjust the margin as needed */
}
</style>
