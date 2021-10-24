<template>
<div>
    <h1>Olá vue</h1>
  <p>Meu nome é {{ nome }}</p>
  <p>Sou {{profissao}}</p>
</div>
</template>

<script>
export default {
  name: "Componente",
  data(){
    return{
      nome: "Andrés",
      profissao: "Dev Front-End"
    }
  }
}
</script>