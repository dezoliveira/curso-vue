<template>
  <img :src="avatar" :alt="descricao">
  <MudarImagem @mudarImagem="trocarImagem"/>
</template>
<script>
import MudarImagem from './MidarImagem.vue'

export default {
  name: 'Picture',
  data(){
    return {
      avatar: "/img/avatar.jpg",
      descricao: "Dart Vader"
    }
  },
  methods: {
    trocarImagem(){
      this.avatar = "/img/avatar2.jpg"
    }
  },
  components:{
    MudarImagem
  }
}
</script>
<style scoped>
  img{
    width: 400px;
  }
</style>