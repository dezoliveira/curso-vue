<template>
  <div>
    <button @click="primeiro(txt1, $event), segundo(txt2, $event)">Ativar MultiplosEventos</button>
    <p>
      {{multiplosEventos}}
    </p>
  </div>
</template>
<script>
export default {
  name: "MultiplosEventos",
  data(){
    return {
      multiplosEventos: "",
      txt1: "Primeiro evento",
      txt2: "Segundo evento"
    }
  },
  methods:{
    primeiro(txt1, e){
      this.multiplosEventos = txt1
    },
    segundo(txt2, e){
      setTimeout(() => this.multiplosEventos = txt2, 500)
    }
  }
}
</script>
<style scoped>
  div{
    margin: 100px;
  }
</style>