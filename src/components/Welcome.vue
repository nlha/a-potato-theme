<template>
  <div class="welcome-wrap">
    <div id="welcome-container" class="welcome-container">

      <div class="welcome-text">
        <h1>Potato is da best!</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Amet, potato.</p>
      </div>

      <div class="potato-bg">
        <div id="potato-img"></div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'Welcome',
  mounted() {
    let welcome = document.querySelector('.welcome-container')
    let textHeading = document.querySelector('.welcome-text h1')
    let textP = document.querySelector('.welcome-text p')
    
    window.addEventListener('scroll', e => {
      if(window.scrollY + 150 > welcome.offsetTop) {
        let floating = (window.scrollY - welcome.offsetTop) / welcome.offsetHeight
        floating = floating.toFixed(1) * 10

        textHeading.style.transform = `translateX(${floating}px)`
        textP.style.transform = `translateX(-${floating}px)`
      }
    })

  }
}
</script>

<style>
  .welcome-container {
    display: flex;
    justify-content: flex-end;
    margin: 1rem;
    padding: 1rem;
  }
  .potato-bg {
    width: 85vw;
    height: 100vh;
  }
  #potato-img {
    background: url('../assets/img/Holiday-Hasselback-Potatoes.jpg') no-repeat center;
    width: 100%;
    height: 100%;
    border-radius: 10px;
    background-size: cover;
  }
  .welcome-text {
    position: absolute;
    top: 40vh;
    left: 5vw;
  }
  .welcome-text h1 {
    font-size: 4rem;
    transition: linear 1000ms;
  }
  .welcome-text p {
    font-size: 1.5rem;
    transition: linear 1000ms;
  }
</style>