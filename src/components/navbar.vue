<template>  
  <nav class="navbar is-transparent is-fixed-top">
    <div class="navbar-brand">
      <router-link to="/" class="navbar-item"><i class="fas fa-home"></i></router-link>     

      <a role="button" class="navbar-burger" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
      </a>
    </div>

    <div clas="navbar-menu">
      <div class="navbar-start">
        <router-link to="/about" class="navbar-item">About</router-link> 
        <router-link to='/hello' class="navbar-item">Hello</router-link> 
      </div>            
    </div>
  </nav>
  
                 
</template>

<script>
export default {
    
}
</script>

<style>
#nav {
  padding: 30px;
  background:#080a0c;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>