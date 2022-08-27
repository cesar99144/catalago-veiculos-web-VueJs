<template>
    <Header />
    <Destaques />
    <Carros />
</template>

<script>

  import Header from '@/components/Header.vue'
  import Veiculos from '@/components/Veiculos.vue'
  import Destaques from '@/components/Destaques.vue';
  import Carros from '@/components/Carros.vue';

  export default {
    name: 'HomeView',
    components:{
      Veiculos,
      Header,
      Destaques,
      Carros
    }
  }
</script>

<style>
  *{
    margin: 0px;
  }

  body{

      background: #F1F1F1;
  }
</style>