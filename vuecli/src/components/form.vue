<template>
<div>
    <form action="" @submit="enviarFormulario($event)">
      <div>
        <input type="text" v-model="name">
      </div>
      <div>
        <input type="text" v-model="email">
      </div>
      <div>
        <submit />
      </div>
  </form>
</div>
</template>
<script>
import inputText from './Form/inputText.vue'
import submit from './Form/submit.vue'
export default {
  name: 'Form',
  components: {
    inputText,
    submit,
  },
  data(){
    return{
      name: "",
      email: ""
    }
  },
  methods:{
    enviarFormulario(e){
      e.preventDefault()

      const name = this.name
      const email = this.email

      console.log("Formulario Enviado!")
      console.log("O nome é " + name)
      console.log("O email é " + email)
    }
  }
}
</script>