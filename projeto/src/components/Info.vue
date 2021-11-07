<template>
  <div>
    <p>Novo email: {{email}}</p>
    <p v-if="esta_trabalhando">Trabalha na Zeeng</p>
    <p v-else>Não esta trabalhando</p>
    <p>Utiliza as principais tecnologias:</p>
    <ul>
      <li
        v-for="(technology, index) in technologies"
        v-bind:key="index"
      >
        {{technology}}
      </li>
    </ul>
    <p>Utiliza os principais frameworks</p>
    <ul>
      <li
        v-for="framework in frameworks"
        :key="framework.id"
      >
        {{framework.framework}}
      </li>
    </ul>
    <div>
      <button @click="showEmail">{{textoBotao}}</button>
    </div>
    <p v-show="mostrar_email">Mande uma mensagem para: {{email}}</p>
    <p class="black">Para acessar meu portfolio <a v-bind:href="meuLink" target="_blank">Clique aqui</a></p>
    <Picture />
  </div>
</template>
<script>
import Picture from './Picture.vue'

export default {
  name: 'Info',
  data(){
    return{
      esta_trabalhando: true,
      mostrar_email: false,
      meuLink: 'https//www.google.com',
      textoBotao: 'Mostrar e-mail',
      technologies: ['HTML', 'CSS', 'Javascipt'], //Array
      frameworks: [
        {id: 1, framework: 'Bootstrap'},
        {id: 2, framework: 'Vue.js'},
      ]//Object
    }
  },
    methods:{
    showEmail(){
      this.mostrar_email = !this.mostrar_email
      if(!this.mostrar_email){
        this.textoBotao = 'Mostrar e-mail'
      }else{
        this.textoBotao = 'Esconder e-mail'
      }
    }
  },
  components:{
    Picture
  },
  props: {
    email: String
  }
}
</script>