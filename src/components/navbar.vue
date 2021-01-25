<template>  

<nav class="navbar" role="navigation" aria-label="main navigation">
  <div class="navbar-brand">
    <a class="navbar-item" href="#">
      <img src="img/rlicon2.png">
    </a>

    <a role="button" class="navbar-burger" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
    </a>
  </div>

  <div id="navbarBasicExample" class="navbar-menu">
    <div class="navbar-start">
         
    </div>

    <div class="navbar-end">
      <a class="navbar-item">
        <router-link to="/" class="navbar-item" style="color:white; font-weight:600;">It's Me</router-link>
      </a>

      <a class="navbar-item">
        <router-link to="/projects" class="navbar-item" style="color:white; font-weight:600;">Projects</router-link> 
      </a>  

      <a class="navbar-item">
        <router-link to='/resume' class="navbar-item" style="color:white; font-weight:600;">Resumé</router-link> 
      </a> 

      <a class="navbar-item">
        <router-link to='/contact' class="navbar-item" style="color:white; font-weight:600;">Contact-me</router-link> 
      </a> 
    </div>
  </div>
</nav>


<!-- <router-link to="/" class="navbar-item"><i class="fas fa-home"></i></router-link> 
<router-link to="/about" class="navbar-item">About</router-link> 
<router-link to='/hello' class="navbar-item">Hello</router-link>  -->
</template>

<script>
export default {
  
}

document.addEventListener('DOMContentLoaded', () => {

  // Get all "navbar-burger" elements
  const $navbarBurgers = Array.prototype.slice.call(document.querySelectorAll('.navbar-burger'), 0);

  // Check if there are any navbar burgers
  if ($navbarBurgers.length > 0) {

    // Add a click event on each of them
    $navbarBurgers.forEach( el => {
      el.addEventListener('click', () => {

        // Get the target from the "data-target" attribute
        const target = el.dataset.target;
        const $target = document.getElementById(target);

        // Toggle the "is-active" class on both the "navbar-burger" and the "navbar-menu"
        el.classList.toggle('is-active');
        $target.classList.toggle('is-active');

      });
    });
  }

});
</script>

<style>
  nav .router-link-active {
    background-color: rgb(51, 50, 61);
  }

  .navbar-item:focus,
  .navbar-item:focus-within,
  .navbar-item:focus-visible {
    background-color: rgb(92, 89, 89) !important;
  }
</style>