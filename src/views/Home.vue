<template>
  <div class="home">

    <div class="columns">
      <div class="column is-8">
        <h1 class="title" style="font-size: 12vh; font-family: sans-serif;">
          {{getMessage('header1')}}
        </h1>
        <h2 class="subtitle" style="font-size: 5vh; font-family: sans-serif;">
          {{getMessage('motto1')}}
        </h2>
      </div>
      <div class="column is-4">
        <img src="img/rlicon2.png" alt="">
      </div>
    </div>
      
  </div>
</template>

<script>
export default {
  name: 'Home',
  components: {
    
  },
  props: ['actuallang'],
  data() {
    return {
      englishText: {
        'header1': "Hello, I'm Richard Lucas",
        'motto1': "I can make the software to solve your problems, so you don't need to."
      },
      brText: {
        'header1': "Olá, eu sou Richard Lucas",
        'motto1': "Eu posso desenvolver o software para resolver o seu problema, assim você não vai precisar fazê-lo."
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
</script>

