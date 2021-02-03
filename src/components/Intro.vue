<template>
  <div class="intro-wrap">
    <div id="intro-container" class="intro-container">

      <div class="intro-text">
        <h1>Everyone loves Potato</h1>
        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Corporis, potato.</p>
      </div>

      <div class="intro-gallery">
        <div id="bg1" class="intro-img bg1"></div>
        <div id="bg2" class="intro-img bg2"></div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'Intro',
  mounted() {
    let intro = document.getElementById('intro-container')
    let bg1 = document.getElementById('bg1')
    let bg2 = document.getElementById('bg2')

    window.addEventListener('scroll', e => {
      if(window.scrollY + 200 > intro.offsetTop && window.scrollY < intro.offsetTop + intro.offsetHeight) {
        let floating = (window.scrollY - intro.offsetTop) / intro.offsetHeight
        floating = floating.toFixed(2) * 20

        bg1.style.transform = `translateX(-${floating}px)`
        bg2.style.transform = `translateX(${floating}px)`
      }
    })
  },
  methods: {
    
  }
}
</script>

<style>
  .intro-wrap {
    width: 100%;
  }
  .intro-container {
    display: flex;
    justify-content: space-between;
    width: 100%;
    height: 100vh;
    padding: 1rem;
  }
  .intro-text {
    position: relative;
    top: 40vh;
    left: 1vw;
    margin: 1rem;
    padding: 1rem;
  }
  .intro-text h1 {
    font-size: 2rem;
  }
  .intro-text p {
    font-size: 1.25rem;
  }
  .intro-gallery {
    display: flex;
    margin: 1rem;
  }
  .intro-img {
    border-radius: 10px;
    overflow: hidden;
    position: relative;
    box-shadow: 1px 1px 3px rgba(0, 0, 0, 0.3);
  }
  .bg1 {
    background: url('../assets/img/Baked-Potato-Wedges.jpg') no-repeat center;
    background-size: cover;
    width: 350px;
    height: 400px;
    top: 25vh;
    z-index: 1;
    transition: linear 1000ms;
  }
  .bg2 {
    background: url('../assets/img/hasselback-potatoes.jpg') no-repeat center;
    background-size: cover;
    width: 400px;
    height: 400px;
    top: 12vh;
    right: 10vw;
    transition: linear 1000ms;
  }
  
</style>