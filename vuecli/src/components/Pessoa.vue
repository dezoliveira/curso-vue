<template>
<div>
  <h2>Pessoa: {{nome}}</h2>
  <p>Nascimento: {{birthday}}</p>
    <p>{{age}} Anos</p>
    <p>Signo: {{zodiac}}</p>
  <Info v-bind:email = "email" v-bind:esta_logado= "true" />
  <Form />
</div>
</template>
<script>
import Form from './form.vue'
import Info from './Info.vue'
export default {
  name: 'Pessoa',
  components: {
    Info,
    Form
  },
  data(){
    return{
      nome: "Andrés",
      birthday: "14/06/1993",
      age: "28",
      zodiac: "Gemini",
      email: "andresoliveira@protonmail.com"
    }
  }
}
</script>