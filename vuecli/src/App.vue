<template>
<div>
  <Header v-bind:esta_logado="true"/>
  <p class="paragrafoPai">Esse é o meu App</p>
  <Componente />
  <LifeCycle />
  <Pessoa />
</div>
</template>

<script>
  import Componente from './components/Componente.vue'
  import LifeCycle from './components/LifeCycle.vue'
  import Pessoa from './components/Pessoa.vue'
  import Header from './components/Header.vue'

  export default {
    name: 'App',
    components:{
      Header,
      Componente,
      LifeCycle,
      Pessoa,
    },
  }
</script>

<style>
body{
    background-color: #333;
    color: #fff;
}

a{
  color: red;
}
</style>