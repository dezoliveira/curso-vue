<template>
  <h2>Formulário:</h2>
  <form action="" @submit="enviarFormulario($event)">
    <label for="">Nome</label>
    <div>
      <input type="text" v-model="name">
    </div>
    <label for="">Email</label>
    <div>
      <input type="text" v-model="email">
    </div>
    <Submit />
  </form>
</template>
<script>
import InputText from './form/InputText.vue'
import Submit from './form/Submit.vue'

export default {
  name: 'Form',
  components:{
    InputText,
    Submit
  },
  data(){
    return {
      name: '',
      email: ''
    }
  },
  methods:{
    enviarFormulario(e){
      e.preventDefault()

      const name = this.name
      const email = this.email

      console.log("Formulário enviado!")
      console.log("O nome é:" + name)
      console.log("O email é: " + email)

    }
  }
}
</script>