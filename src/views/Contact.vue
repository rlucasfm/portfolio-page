<template>
    <div class="contact">
        <div class="columns">
            <div class="column is-4">
                <img src="img/rlicon2.png" alt="">
            </div>
            <div class="column">
                <h1 class="title mt-5" style="font-size: 8vh; font-family: sans-serif;">{{getMessage('header1')}}</h1>
            </div>
        </div>
        <div class="columns">
            <div class="column is-3">
                <a href="https://www.linkedin.com/in/richard-lucas-furtado-de-mendonca/" target="_blank" class="fa fa-linkedin animated"></a>                                
            </div>            
            <div class="column is-3">
                <a href="mailto:richardlucasfm@gmail.com?Subject=Ol%E1%21%20Vi%20o%20seu%20portfolio&Body=Gostaria%20de%20saber%20mais%20sobre%20o%20seu%20trabalho" target="_blank" class="fa fa-google animated"></a>                
            </div>                       
            <div class="column is-3">
                <a href="https://www.facebook.com/richardlucasfm/" target="_blank" class="fa fa-facebook animated"></a>                
            </div>      
            <div class="column is-3">
                <a href="https://github.com/rlucasfm" target="_blank" class="fab fa-github animated"></a>
            </div>      
        </div>
    </div>
</template>

<style>
.animated {
    animation: pulse 3s infinite;
    animation-direction: alternate;
}
@keyframes pulse {
    100% {
        transform: translateY(20px);
    }
}

.fa-github {
    color: white;
    font-size: 14vh;    
    text-align: center;
    text-decoration: none;
    border-radius: 50%;
    transition: transform 0.7s; 
}
.fab:hover {
    color: white;
    transform: scale(1.2);
}

.fa {
    padding: 20px;
    font-size: 8vh;    
    text-align: center;
    text-decoration: none;
    border-radius: 50%;
    transition: transform 0.7s;
}

.fa:hover {
    transform: scale(1.2);
}

.fa-google {
    background-color: #dd4b39;
    color: white;
}
.fa-google:hover{
    color: white;
}

.fa-linkedin {
    background-color: #007bb5;
    color: white;
}
.fa-linkedin:hover {
    color: white;
}

.fa-facebook {
    width: 13vh;
    background-color: #3B5998;
    color: white;
}
.fa-facebook:hover {
    color: white;
}
</style>

<script>
export default {
    props: ['actuallang'],
  data() {
    return {
      englishText: {
        'header1'   : "Through this channels you will be able to know me better and my job as well!",
      },
      brText: {
        'header1'   : "Através destes canais você poderá conhecer melhor a mim e ao meu trabalho!",
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