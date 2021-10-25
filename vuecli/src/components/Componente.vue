<template>
<div>
  <h1>Olá vue</h1>
  <p>Meu nome é {{ nome }}</p>
  <p>Sou {{profissao}}</p>
  <small>Trabalho na {{work}}</small>
  <MultiplosEventos />
  <Reutilizacao />
  <Reutilizacao />
  <Reutilizacao />
</div>
</template>

<script>
import MultiplosEventos from './MultiplosEventos.vue'
import Reutilizacao from './Reutilizacao.vue'
export default {
  name: "Componente",
  components: {
    MultiplosEventos,
    Reutilizacao
  },
  data(){
    return{
      nome: "Andrés",
      profissao: "Dev Front-End",
      work: "Zeeng"
    }
  },
}
</script>