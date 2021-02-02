<template>
  <div class="video-wrap">
    <div class="video-container">

      <div class="video-bg"></div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'Video'
}
</script>

<style>
  .video-wrap {
    width: 100%;
  }
  .video-container {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100vh;
    padding: 1rem;
  }
  .video-bg {
    background: url('../assets/img/frenchfries.jpg') no-repeat center;
    background-size: cover;
    height: 90%;
    width: 90%;
    border-radius: 10px;
  }
</style>