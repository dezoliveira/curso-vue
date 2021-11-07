<template>
  <h1>Meu nome é: {{nome}}</h1>
</template>
<script>
export default {
  name: 'LifeCycle',
  data(){
    return{
      nome: "Ciclo de vida do componente"
    }
  },
  created(){
    setTimeout(() =>{
      this.nome = "Created"
    }, 1000)

    this.lifeCycle()
  },
  mounted(){
    setTimeout(()=>{
      this.nome = "Mounted"
    }, 2000)
  },
  methods:{
    lifeCycle(){
      console.log("Executou")
    }
  }
}
</script>