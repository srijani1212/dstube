<template>
  <div class="main">
    <div class="card-container">
      <!-- Loop through the videoList array and render cards -->
      <Card v-for="video in videoList" :key="video.id" 
        :image="video.imgSrc" 
        :title="video.title" 
        :description="video.desc" 
        :creator="video.creator.firstname + ' ' + video.creator.lastname" 
        :viewCount="video.views" 
      />
    </div>
  </div>
</template>

<script>
import Card from './Card.vue'; // Import the Card component

export default {
  components: {
    Card, // Register the Card component
  },
  data() {
    return {
      videoList: [], // Initialize an empty array to hold the video data
    };
  },
  mounted() {
    // Load the video data from your data.json file
    this.loadVideoData();
  },
  methods: {
    async loadVideoData() {
      try {
        // Fetch the video data from your data.json file or an API endpoint
        const response = await fetch('..assets/data.json');
        const data = await response.json();
        this.videoList = data; // Assign the data to the videoList array
      } catch (error) {
        console.error('Error loading video data:', error);
      }
    },
  },
};
</script>

<style scoped>
/* Your styling for the main content and card container goes here */
</style>
