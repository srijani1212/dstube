<template>
  <div class="parent-container">
    <header-container></header-container>
    <div class="main-container">
      <div class="videos" style="margin-top: 145px;">
        <div v-for="video in videos" :key="video.id" class="video-card">
          <div class="thumbnail">
            <img :src="video.imgSrc" alt="Video Thumbnail" />
          </div>
          <div class="video-info">
            <h2>{{ video.title }}</h2>
            <div class="views">{{ video.views }} views </div>
            <div class="creator">{{ video.creator.firstname }} {{ video.creator.lastname }}</div>
            <div class="description">{{ video.desc }}</div>
            <button class="remove-button" @click="removeVideo(video.id)">REMOVE</button>
          </div>
        </div>
      </div>
    </div> <!-- Close main-container -->
  </div>
</template>

<script>
import videoData from "../assets/data.json";

export default {
  data() {
    return {
      videos: videoData,
    };
  },
  methods: {
    removeVideo(videoId) {
      this.videos = this.videos.filter((video) => video.id !== videoId);
    },
  },
};
</script>

<style scoped>
body {
  margin: 0;
  padding: 0;
  background-color: #000; /* Set black background for the entire page */
  color: #fff; /* Set white text color */
}
.parent-container {
  position: relative;
}

header-container {
  background-color: #333;
  color: #fff;
  padding: 20px;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 2;
  margin: 0; /* Remove margin to eliminate gap */
}

main-container {
  background-color: #000; /* Set black background for the main container */
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1;
}

.videos {
  display: flex;
  flex-direction: column;
  background-color: #000;
}

.video-card {
  margin-left: 20px; /* Add a gap from the left */
  margin-top: 20px; /* Add a gap from the top */

  height: 261.96px;
  margin-bottom: 20px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  display: flex;
  border: 1px solid #000;
}

.thumbnail {
  flex: 1;
  padding-right: 10px;
  align-items: flex-end;
}

.thumbnail img {
  width: 100%;
  height: 100%;
}

.video-info {
  flex: 2;
  padding: 10px;
  color: white;
}

.video-info h2 {
  font-size: 1.25rem;
  margin: 0;
  color: white;
  margin-bottom: 10px;
}

.views {
  font-size: 1rem;
  margin: 0;
  color: #666;
  margin-bottom: 10px;
}
.creator{
  margin-bottom:40px;
}
.description {
  font-size: 1rem;
  margin: 0;
  color: white;
  margin-bottom: 50px;
}

.remove-button {
  width: 104px;
  height: 34px;
  border-radius: 4px;
  border: 1px solid #fff;
  background-color: transparent;
  color: #fff;
  font-family: Roboto;
  font-size: 16px;
  font-weight: 700;
  line-height: 19px;
  letter-spacing: 0em;
  text-align: left;
  cursor: pointer;
}
</style>
