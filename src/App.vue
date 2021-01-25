<template>
<section class="hero is-black is-bold is-fullheight">
  <!-- Hero head: will stick at the top -->
  <div class="hero-head">
    <div class="container">
      <navbar :actuallang="message" @change-lang='changelang'/>
    </div>
  </div>

  <div class="hero-body">
    <div class="container">
      <router-view v-slot="{ Component }" :actuallang="message">
        <transition name="slide" mode="out-in">
          <component :is="Component" />
        </transition>
      </router-view>

    </div>
  </div>
  
</section>
</template>

<script>
import navbar from '@/components/navbar.vue'

export default {
  data () {
    return {
      message: 'EN'
    }
  },
  methods: {
    changelang(){
      if(this.message == 'EN'){
        this.message = 'PT'
      }else{
        this.message = 'EN'
      }
    }
  },
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
