<template>
  <div>
    <p>{{email}}</p>
    <p v-if="esta_trabalhando">Andrés está trabalhando no momento com:</p>
    <p v-else>Andrés não está trabalhando com:</p>
    <div>
      <button @click="showEmail">{{textoBotao}}</button>
    </div>
    <p>Skills:</p>
    <ul>
      <li  v-for="(technology, index) in technologies" v-bind:key="index">{{technology}}</li>
    </ul>
    <p>Frameworks:</p>
    <ul>
      <li v-for="framework in frameworks" v-bind:key="framework.id">
        {{framework.language}}
      </li>
    </ul>
    <p v-show="mostrar_email">Mande uma mensagem para: {{email}}</p>
    <p>Para acessar meu portfolio <a v-bind:href="meuLink" target="_blank"> basta clicar aqui </a> </p>
    <Picture />
  </div>
</template>
<script>
import Picture from './Picture.vue'
export default {
  name: 'Info',
  components: { 
    Picture
  },
  props:{
    email: String
  },
  data(){
    return{
      esta_trabalhando: true,
      mostrar_email: false,
      meuLink: 'https:\\www.google.com',
      textoBotao: 'Mostrar e-mail',
      technologies: ["HTML", "CSS", "Javascript"],
      frameworks: [
        {id: 1, language: 'Bootstrap'},
        {id: 2, language: 'Vue.js'},
      ]
    }
  },
  methods: {
    showEmail(){
      this.mostrar_email = !this.mostrar_email
      if(!this.mostrar_email){
        this.textoBotao = 'Mostrar email'
      }else{
        this.textoBotao = 'Botão escondido'
      }
    }
  }
}
</script>

<style>
  .paragrafoPai{
    color: aqua;
  }
</style>