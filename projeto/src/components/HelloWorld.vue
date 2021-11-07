<template>
  <h1>Hello World</h1>
  <p>Meu nome é {{name}}</p>
  <p>Eu sou {{work}}</p>
  <MultiplosEventos />
  <Reutilizacao />
  <Reutilizacao />
  <Reutilizacao />
</template>
<script>
import MultiplosEventos from './MultiplosEventos.vue'
import Reutilizacao from './Reutilizacao.vue'

export default {
  name:"HelloWorld",
  data(){
    return {
      name: "Andrés",
      work: "Dev"
    }
  },
  components:{
    MultiplosEventos,
    Reutilizacao
  }
}
</script>