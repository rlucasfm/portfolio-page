<template>  

<nav class="navbar" role="navigation" aria-label="main navigation">
  <div class="navbar-brand">
    <a class="navbar-item" href="#">
      
    </a>

    <a role="button" class="navbar-burger" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
    </a>
  </div>

  <div id="navbarBasicExample" class="navbar-menu">
    <div class="navbar-start">
         <button class="button navbar-item mt-2 ml-2" id="btnlang" style="background-color: black" @click="$emit('changeLang')">{{actuallang}}</button>
    </div>

    <div class="navbar-end">            

      <a class="navbar-item">
        <router-link to="/" class="navbar-item" style="color:white; font-weight:600;">{{getMessage('menu1')}}</router-link>
      </a>

      <a class="navbar-item">
        <router-link to="/projects" class="navbar-item" style="color:white; font-weight:600;">{{getMessage('menu2')}}</router-link> 
      </a>  

      <a class="navbar-item">
        <router-link to='/knowme' class="navbar-item" style="color:white; font-weight:600;">{{getMessage('menu3')}}</router-link> 
      </a> 

      <a class="navbar-item">
        <router-link to='/contact' class="navbar-item" style="color:white; font-weight:600;">{{getMessage('menu4')}}</router-link> 
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
  props: ['actuallang'],
  data() {
    return {
      message: 'EN',
      englishText: {
        'menu1': "It's me",
        'menu2': "Projects",
        'menu3': "Know me better",
        'menu4': "Contact-me"
      },
      brText: {
        'menu1': "Sou eu",
        'menu2': "Projetos",
        'menu3': "Me conheça melhor",
        'menu4': "Entre em contato"
      }
    }
  },
  methods: {
    getMessage(textContext){
      if(this.actuallang == 'EN'){
        return this.englishText[textContext]
      }else{
        return this.brText[textContext]
      }
    }
  }
}

document.addEventListener('DOMContentLoaded', () => {

  // Get all "navbar-burger" elements
  const $navbarBurgers = Array.prototype.slice.call(document.querySelectorAll('.navbar-burger'), 0);

  localStorage.setItem('lang', 'EN');
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