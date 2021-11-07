<template>
  <Header />
  <HelloWorld />
  <LifeCycle />
  <Pessoa />
</template>
<script>
import HelloWorld from './components/HelloWorld.vue'
import LifeCycle from './components/LifeCycle.vue'
import Pessoa from './components/Pessoa.vue'
import Header from './components/Header.vue'

export default {
  name: "App",
  components: {
    HelloWorld,
    LifeCycle,
    Pessoa,
    Header
  }
}
</script>
<style>
  body{
    background-color: #333;
    color: #FFF;
  }
  a {
    color: red;
  }

  .black {
    background-color: #000;
  }
</style>