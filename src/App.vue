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

<style lang="scss">
@import '~bulma/css/bulma.css';
</style>
