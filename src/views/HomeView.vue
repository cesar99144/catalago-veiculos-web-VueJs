<template>
    <Header />
    <Destaques />
</template>

<script>

  import Header from '@/components/Header.vue'
  import Veiculos from '@/components/Veiculos.vue'
  import Destaques from '@/components/Destaques.vue';

  export default {
    name: 'HomeView',
    components:{
      Veiculos,
      Header,
      Destaques
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