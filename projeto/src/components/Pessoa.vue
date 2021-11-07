<template>
  <h2>Descrição da Pessoa: {{nome}}</h2>
  <Info :email="email"/>
  <Form />
</template>
<script>
import Info from './Info.vue'
import Form from './Form.vue'

export default {
  name: "Pessoa",
  data(){
    return{
      nome: 'Andrés',
      email: 'andresoliveira@protonmail.com'
    }
  },
  components:{
    Info,
    Form
  }
}
</script>