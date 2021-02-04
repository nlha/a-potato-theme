<template>
  <div class="facts-wrap">
    <div class="facts-container">

      <div id="percent-wrap" class="percent-wrap"><span>{{ percentage }}.{{ fraction }}%</span> fat-free.</div>
      <p>Potato contains vitamin B6, potassium, and more.</p>

    </div>
  </div>
</template>

<script>
export default {
  name: 'Facts',
  data() {
    return {
      percentage: 0,
      fraction: 0
    }
  },
  mounted() {
    let facts = document.querySelector('.facts-container')
    let percentText = document.querySelector('.percent-wrap')

    window.addEventListener('scroll', e => {
      if(window.scrollY + 200 >= facts.offsetTop) {
        facts.style.animation = 'slideIn linear 1000ms forwards'
      }
      if(window.scrollY == facts.offsetTop) {
        this.startTimer()
      }
    })
  },
  methods: {
    startTimer() {
      if(this.percentage < 99 && this.fraction < 9) {
        let timer = setInterval(() => {
          this.fraction++
          if(this.fraction > 9) {
            this.fraction = 0
            this.percentage++
          }
          if(this.percentage >= 99 && this.fraction >= 9) {
            clearInterval(timer)
          }
        }, 0)
      }
    }
  }
}
</script>

<style>
  .facts-wrap {
    width: 100%;
    background-color: #F6ECDA;
    display: flex;
  }
  .facts-container {
    width: 100%;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    opacity: 0;
  }
  .facts-container p {
    font-size: 2rem;
  }
  .percent-wrap {
    font-size: 3rem;
  }
  .percent-wrap span {
    font-size: 10rem;
    color: burlywood;
  }
  @keyframes slideIn {
    0% {
      transform: translateY(-50%);
      opacity: 0;
    }
    100% {
      transform: translateY(0);
      opacity: 100%;
    }
  }
</style>