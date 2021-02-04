<template>
  <div class="footer-wrap">
    <div class="footer-container">

      <div class="footer-text">
        <h2>A Potato Webpage</h2>
        <p>by a potato lover.</p>
        <div class="social-links">
          <div class="social"><i class="fab fa-twitter"></i></div>
          <div class="social"><i class="fab fa-facebook-f"></i></div>
          <div class="social"><i class="fab fa-instagram"></i></div>
          <div class="social"><i class="fab fa-google-plus-g"></i></div>
        </div>
      </div>

      <div class="copyright">&#169; All Right Reserves. Design by Han.</div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style>
  .footer-wrap {
    width: 100%;
    height: 100vh;
    background: #744529;
  }
  .footer-container {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  .footer-text {
    margin-top: 100px;
    color: burlywood;
    flex-grow: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .footer-text h2 {
    font-size: 4rem;
  }
  .footer-text p {
    font-size: 1.5rem;
  }
  .social-links {
    display: flex;
    margin-top: 20px;
    padding: 10px;
    justify-content: center;
    align-items: center;
  }
  .social {
    color: burlywood;
    margin: 20px;
    font-size: 2rem;
    cursor: pointer;
  }
  .social:hover {
    color: #F6ECDA;
    transform: scale(1.2);
    transition: linear 300ms;
  }
  .copyright {
    padding: 60px 120px;
    color: #F6ECDA;
    background: #633720;
    font-size: 1.25rem;
    
  }
</style>