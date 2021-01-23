<template>
  <navbar/>
  <router-view/> 
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
  body {
    background-color: rgb(43, 44, 54);
    overflow: hidden;
  }
</style>

<style lang="scss">
@import '~bulma/css/bulma.css';
</style>
