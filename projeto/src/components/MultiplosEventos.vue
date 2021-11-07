<template>
  <div>
    <button @click="primeiro($event), segundo($event)">
      Ativar Multiplos Eventos
    </button>
    <p>{{multiplosEventos}}</p>
  </div>
</template>
<script>
export default {
  name: "MultiplosEventos",
  data(){
    return{
      multiplosEventos: ""
    }
  },
  methods:{
    primeiro(e){
      this.multiplosEventos = "Primeiro evento!"
    },
    segundo(e){
      setTimeout(() => this.multiplosEventos = "Segundo evento!", 500)
    }
  }

}
</script>
<style scoped>
  div{
    margin: 100px;
  }
</style>