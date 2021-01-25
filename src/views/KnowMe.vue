<template>
    <div class="hello">
        <div class="columns">

            <div class="column is-4">
                <img src="img/rlicon2.png" alt="">
            </div>

            <div class="column">
                <h1 class="title" style="font-size: 8vh; font-family: sans-serif;">{{getMessage('header1')}}</h1>   
                <p style="font-family: sans-serif; font-weight: bold;">{{getMessage('desc1')}}</p> 
                <br>
                <p style="font-family: sans-serif; font-weight: bold;">{{getMessage('desc2')}}</p>   
                <br>
                <p style="font-family: sans-serif; font-weight: bold;">{{getMessage('desc3')}}</p>                                        
            </div>
            

        </div>
    </div>
</template>

<script>
export default {
    props: ['actuallang'],
  data() {
    return {
      englishText: {
        'header1'   : "I'm a developer!",
        'desc1'     : "With more than 6 years on developing programming skills, technician in Industrial Automation by one of the most respected Technical Institutes on Brazil, Instituto Federal de Ciência, Educação e Tecnologia do Maranhão, and Electrical Engineer in the same instutite.",
        'desc2'     : "Inherited (My life is OOP!) the love for development and programming from my dad, who ignited in me the wish to travel on this learning journey, even influencing me in learning Delphi bakc in the days.",
        'desc3'     : "Always learning more technologies and trying to stay on the top of what is the state-of-the-art in development. Nowadays working with JavaScript (With techonlogies like NodeJS and frameworks/libraries like VueJS, jQuery...), PHP (Including frameworks like Laravel and Code Igniter 4), Python (Mostly for Data Science and Machine Learning with TensorFlow, Pandas, SciPy...) and what most be needed for solving the problem!"
      },
      brText: {
        'header1'   : "Eu sou um desenvolvedor!",
        'desc1'     : "Com mais de 6 anos desenvolvendo habilidades de programação, técnico em Automação Industrial por um dos mais conceituados Institutos Técnicos do Brasil, o Instituto Federal de Ciência, Educação e Tecnologia do Maranhão, e Engenheiro Eletricista na mesma instituição.",
        'desc2'     : "Herdei (minha vida é OOP!) o amor por desenvolvimento e programação de meu pai, que despertou em mim o desejo de viajar nessa jornada de aprendizado, até mesmo me influenciando no aprendizado do Delphi há tempos atrás.",
        'desc3'     : "Sempre aprendendo mais tecnologias e procurando ficar por dentro do que há de mais moderno em desenvolvimento. Atualmente trabalhando com JavaScript (com tecnologias como NodeJS e frameworks / bibliotecas como VueJS, jQuery...), PHP (incluindo frameworks como Laravel e Code Igniter 4), Python (principalmente para Data Science e Machine Learning com TensorFlow, Pandas, SciPy...) e o que mais for preciso para resolver o problema!"
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
