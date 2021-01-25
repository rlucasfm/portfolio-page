<template>
  <div class="about">
    <div class="columns">

      <div class="column is-4">
        <div class="card">
          <div class="card-image">
            <figure class="image is-4by3">
              <img src="img/em1.jpg" alt="Placeholder image">
            </figure>
          </div>
          <header class="card-header">
            <p class="card-header-title">{{getMessage('title1')}}</p>
          </header>
          <div class="card-content">            
            <div class="content">
              {{getMessage('desc1')}}
              <br><br>
              <small><span class="PHP"></span> PHP</small>           
            </div>
          </div>
        </div>
      </div>

      <div class="column is-4">
        <div class="card">
          <div class="card-image">
            <figure class="image is-4by3">
              <img src="img/indev.jpg" alt="Placeholder image">
            </figure>
          </div>
          <header class="card-header">
            <p class="card-header-title">{{getMessage('title2')}}</p>
          </header>
          <div class="card-content">            
            <div class="content">              
              {{getMessage('desc2')}}
              <br>
              <small>{{getMessage('small2')}}</small> 
              <br><br>
              <small><span class="NodeJS"></span> NodeJS</small>             
            </div>
          </div>
        </div>
      </div>

       <div class="column is-4">
        <div class="card">
          <div class="card-image">
            <figure class="image is-4by3">
              <img src="img/sound.jpg" alt="Placeholder image">
            </figure>
          </div>
          <header class="card-header">
            <p class="card-header-title">{{getMessage('title3')}}</p>
          </header>
          <div class="card-content">            
            <div class="content">              
              {{getMessage('desc3')}}
              <br><br>
              <small><span class="Python"></span> Python</small>               
            </div>
          </div>
        </div>
      </div>      
    </div>
    <div class="columns">

      <div class="column is-4">
        <div class="card">
          <div class="card-image">
            <figure class="image is-4by3">
              <img src="img/food.png" alt="Placeholder image">
            </figure>
          </div>
          <header class="card-header">
            <p class="card-header-title">{{getMessage('title4')}}</p>
          </header>
          <div class="card-content">            
            <div class="content">
              {{getMessage('desc4')}}
              <br>
              <small><span class="Python"></span> Python</small>               
            </div>
          </div>
        </div>
      </div>
      <div class="column is-4">
        <div class="card">
          <div class="card-image">
            <figure class="image is-4by3">
              <img src="img/api.png" alt="Placeholder image">
            </figure>
          </div>
          <header class="card-header">
            <p class="card-header-title">{{getMessage('title5')}}</p>
          </header>
          <div class="card-content">            
            <div class="content">
              {{getMessage('desc5')}}
              <br><br>
              <small><span class="Delphi"></span >Delphi</small>               
            </div>
          </div>
        </div>
      </div>

      <div class="column is-4">
        <div class="card">
          <div class="card-image">
            <figure class="image is-4by3">
              <img src="img/rlicon2.png" alt="Placeholder image">
            </figure>
          </div>
          <header class="card-header">
            <p class="card-header-title">{{getMessage('title6')}}</p>
          </header>
          <div class="card-content mb-5">            
            <div class="content">
              {{getMessage('desc6')}}             
            </div>
          </div>
        </div>
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
        'title1'  : "Emergência1",
        'desc1'   : "Online course platform with integration with online selling platforms like Braip, Monetizze, Hotmart and others.",
        'title2'  : "Scholar Management",
        'desc2'   : 'Scholar management and automated diary system.',
        'small2'  : 'In development',
        'title3'  : 'Sound analysis system',
        'desc3'   : 'System applying artificial inteligence techniques to evaluate sound emissors quality.',
        'title4'  : 'Stock and register management system',
        'desc4'   : 'Web Software made with Django framework for restaurants and food mercs, with eletronic register integrated with stock control.',
        'title5'  : 'API DataSnap',
        'desc5'   : 'DataSnap build API, in Delphi as integration between web CodeIgniter (PHP) and CRM system in Delphi',
        'title6'  : 'And others...',
        'desc6'   : 'Lots of softwares and sites build with tools in PHP like CodeIgniter 4, JavaScript like NodeJS, frameworks front-end like VueJS, Bulma and Bootstrap'
      },
      brText: {
        'title1'  : "Emergência1",
        'desc1'   : "Plataforma de cursos online com integração com plataformas de venda online como Braip, Monetizze, Hotmart e outros",
        'title2'  : "Gestão escolar",
        'desc2'   : 'Sistema de diários eletrônicos e gestão escolas.',
        'small2'  : 'Em desenvolvimento',
        'title3'  : 'Sistema de análise sonora',
        'desc3'   : 'Sistema aplicando tecnicas de inteligência artifical para avaliar a qualidade de emissores sonoros',
        'title4'  : 'Gestão de estoque e comandas eletronicas',
        'desc4'   : 'Sistema web feito com framework Django para restaurantes e lanchonetes, com sistema de comanda eletrônicas integrado a controle de estoque',
        'title5'  : 'API DataSnap',
        'desc5'   : 'API feita em DataSnap, em Delphi como integração entre sistema web CodeIgniter (PHP) e um sistema CRM em Delphi.',
        'title6'  : 'Entre outros...',
        'desc6'   : 'Diversos softwares e sites feitos com ferramentas PHP like CodeIgniter 4, Javascript como NodeJS, frameworks front-end como VueJS, Bulma e Bootstrap'
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
</script>script>

<style>
  .PHP {
  height: 10px;
  width: 10px;
  background-color: rgb(47, 49, 179);
  border-radius: 50%;
  display: inline-block;
}

.NodeJS {
  height: 10px;
  width: 10px;
  background-color: rgb(238, 163, 66);
  border-radius: 50%;
  display: inline-block;
}

.Python {
  height: 10px;
  width: 10px;
  background-color: rgb(31, 7, 167);
  border-radius: 50%;
  display: inline-block;
}

.Delphi {
  height: 10px;
  width: 10px;
  background-color: rgb(98, 192, 21);
  border-radius: 50%;
  display: inline-block;
}

.card {
  background-color: transparent;
  color: white;
  border-style: solid;
  border-color: white;
  border-width: thin;
  transition: transform 1s;
  transition: color 1s;
  transition: background-color 1s;
}
.card:hover{
  background-color: white;
  color: black;
  transform: scale(1.1);  
  z-index: 100;
}

.card-header-title {
  color: white;  
  transition: color 1s;
}

.card:hover .card-header-title {
  color: black;
}
</style>
