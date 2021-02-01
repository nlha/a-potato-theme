<template>
  <div class="navbar-wrap">
    <div class="navbar-container">

      <div class="nav-logo">Potato</div>

      <div class="nav-links-container">
        <ul class="nav-links">
          <li><a href="#">Home</a></li>
          <li><a href="#">About</a></li>
          <li><a href="#">Pages</a></li>
          <li><a href="#">Contact</a></li>
        </ul>
      </div>
      
    </div>
  </div>
</template>

<script>
export default {
  name: 'Navbar'
}
</script>

<style>
  * {
    margin: 0;
    box-sizing: border-box;
  }
  .navbar-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 1.5rem;
    border-bottom: 0.1rem solid black;
  }
  .nav-logo {
    font-size: 2.5rem;
    padding: 1.25rem;
    text-shadow: 1px 0 0 burlywood;
  }
  .nav-links {
    display: flex;
    justify-content: space-evenly;
    font-size: 1.5rem;
  }
  .nav-links li {
    list-style-type: none;
    padding: 1.25rem;
  }
  .nav-links li a {
    text-decoration: none;
    color: black;
  }
  .nav-links li a:hover {
    color: burlywood;
  }
  
</style>