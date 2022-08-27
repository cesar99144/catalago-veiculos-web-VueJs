<template>
    <Header />
    <Destaques />
    <Carros />
    <Motos />
    <Consultores />
</template>

<script>

  import Header from '@/components/Header.vue'
  import Destaques from '@/components/Destaques.vue';
  import Carros from '@/components/Carros.vue';
  import Motos from '@/components/Motos.vue';
  import Consultores from '@/components/Consultores.vue';

  export default {
    name: 'HomeView',
    components:{
      Header,
      Destaques,
      Carros,
      Motos,
      Consultores
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