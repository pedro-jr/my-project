<template>
  <div>
    <p>Loja de Livros</p>
    <Cadastro/>
    
  </div>
</template>

<script>

import Cadastro from "./components/Cadastro.vue";

export default {
  name: 'App',
  components: {
    Cadastro
  }
}
</script>

<style scoped>
  p{
    text-align: center;
  }
</style>
