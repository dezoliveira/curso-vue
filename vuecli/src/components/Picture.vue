<template>
<div>
  <img class="anonymous" v-bind:src="avatar" v-bind:alt="descricao">
  <MudarImagem @mudar-imagem="trocarImagem" />
</div>
</template>
<script>
import Reutilizacao from './Reutilizacao.vue'
import MudarImagem from './MudarImagem.vue'

export default {
  name: "Picture",
  components:{
    Reutilizacao,
    MudarImagem
  },
  data(){
    return{
      avatar: "/img/fawkes.jpg",
      descricao: "Anonimous"
    }
  },
  methods:{
    trocarImagem(){
      this.avatar = "/img/flame.jpg"
    }
  }
}
</script>

<style scoped>
.anonymous{
  width: 400px;
  margin: 15px;  
}
</style>
