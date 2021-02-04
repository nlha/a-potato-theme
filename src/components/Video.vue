<template>
  <div class="video-wrap">
    <div class="video-container">

      <div class="bg-wrap">
        <div class="video-bg"></div>

        <div class="bg-text" @click="toggleVideo">
          <h1>Tasty FrenchFries</h1>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis, potato.</p>
        </div>
      </div>

      <div class="video-clip" @click="toggleVideo">
        <iframe id="video" width="560" height="315" src="https://www.youtube.com/embed/gVRyWnClItc" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'Video',
  methods: {
    toggleVideo() {
      let showVid = document.querySelector('.video-clip')
      let video = document.querySelector('#video')

      showVid.classList.toggle('active')
      video.setAttribute('src', 'https://www.youtube.com/embed/gVRyWnClItc')
    }
  }
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
    background-color: #FBF6ED;
  }
  .bg-wrap {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 90%;
    height: 100vh;
  }
  .video-bg {
    background: url('../assets/img/frenchfries.jpg') no-repeat center;
    background-size: cover;
    height: 90%;
    width: 100%;
    border-radius: 10px;
  }
  .bg-text {
    background-color: rgb(0, 0, 0);
    background-color: rgba(0, 0, 0, 0.4);
    color: white;
    font-weight: bold;
    border: 3px solid burlywood;
    position: absolute;
    z-index: 2;
    width: 80%;
    padding: 20px;
    text-align: center;
    cursor: pointer;
    opacity: 0;
  }
  .bg-wrap:hover .video-bg {
    filter: blur(8px);
    -webkit-filter: blur(8px);
    transition: 1000ms linear;
  }
  .bg-wrap:hover .bg-text {
    opacity: 1;
    transition: 500ms linear;
  }
  .video-clip {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: 10000;
    background: rgba(0, 0, 0, 0.9);
    width: 100vw;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    opacity: 0;
    visibility: hidden;
  }
  .video-clip.active {
    opacity: 1;
    visibility: visible;
  }
  #video {
    position: relative;
    max-width: 900px;
    outline: none;
  }
  @media (max-width: 991px) {
    #video {
      max-width: 90%;
    }
  }
</style>