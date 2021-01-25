<template>
<section class="hero is-black is-bold is-fullheight">
  <!-- Hero head: will stick at the top -->
  <div class="hero-head">
    <div class="container">
      <navbar/>
    </div>
  </div>

  <div class="hero-body">
    <div class="container">
      <transition name="slide" mode="out-in">
        <router-view :key="$route.path"/> 
      </transition>      
    </div>
  </div>
  
</section>
</template>

<script>
import navbar from '@/components/navbar.vue'

export default {
  components: {
    navbar
  }
}
</script>

<style>
body::-webkit-scrollbar {
    display: none;
}

/* Hide scrollbar for IE, Edge and Firefox */
body {
  -ms-overflow-style: none;  /* IE and Edge */
  scrollbar-width: none;  /* Firefox */
}

.slide-enter-active,
.slide-leave-active {
  transition: opacity 1s, transform 1s;
}

.slide-enter,
.slide-leave-to {
  opacity: 0;
  transform: translateX(-30%);
}
</style>

<style lang="scss">
@import '~bulma/css/bulma.css';
</style>
