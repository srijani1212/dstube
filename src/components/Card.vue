<template>
    <div class="card">
      <img :src="image" alt="Card Image" class="card-image" />
      <div class="card-details">
        <h3 class="card-title">{{ title }}</h3>
        <p class="card-description">{{ description }}</p>
        <p class="card-creator">{{ creator }}</p>
        <p class="card-views">{{ viewCount }} Views</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      image: String,
      title: String,
      description: String,
      creator: String,
      viewCount: Number,
    },
  };
  </script>
  
  <style scoped>
  .card {
    width: 1358px;
    height: 261.96px;
    position: absolute;
    top: 186.52px;
    left: 45px;
    background: #181818;
    border: 1px solid #ccc;
    border-radius: 8px;
    display: flex;
    margin: 16px;
    padding: 16px;
  }
  
  .card-image {
    width: 469px;
    height: 261.96px;
    top: 186.52px;
    left: 45px;
  }
  
  .card-details {
    flex-grow: 1;
  }
  
  .card-title {
    width: 855px;
    height: 22.4px;
    top: 198.21px;
    left: 525px;
    font-family: Roboto;
    font-size: 20px;
    font-weight: 400;
    line-height: 23px;
    letter-spacing: 0em;
    text-align: left;
    background: #FFFFFF;
    margin: 0;
    padding: 8px; /* Add padding for spacing */
  }
  
  .card-description {
    width: 838px;
    height: 77px;
    top: 353px;
    left: 525px;
    font-family: Roboto;
    font-size: 16px;
    font-weight: 400;
    line-height: 19px;
    letter-spacing: 0em;
    text-align: left;
    background: #FFFFFF;
    padding: 8px; /* Add padding for spacing */
    margin: 0;
  }
  
  .card-creator {
    width: 855px;
    height: 44.8px;
    top: 318px;
    left: 525px;
    font-family: Roboto;
    font-size: 20px;
    font-weight: 400;
    line-height: 23px;
    letter-spacing: 0em;
    text-align: left;
    background: #FFFFFF;
    margin: 0;
    padding: 8px; /* Add padding for spacing */
  }
  
  .card-views {
    width: 855px;
    height: 18.5px;
    top: 235.21px;
    left: 525px;
    font-family: Roboto;
    font-size: 16px;
    font-weight: 400;
    line-height: 19px;
    letter-spacing: 0em;
    text-align: left;
    background: #FFFFFF;
    margin: 0;
    padding: 8px; /* Add padding for spacing */
  }
  </style>
  