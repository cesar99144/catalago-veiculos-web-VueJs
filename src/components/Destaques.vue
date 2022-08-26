<template>
    <div class="section-content">
        <h3 class="titulo-content">Veículos em destaque</h3>

        <div id="areaDadosCard">
            <CardVeiculos titulo="gol g6"/>
            <CardVeiculos titulo="Fiat uno" imagem="http://localhost:8081/arquivosImagens/60b23a8a491fe.png" class="cardItem" />
            <CardVeiculos titulo="gol g6" imagem="http://localhost:8081/arquivosImagens/60b047ca1c6b9.jpg" class="cardItem" />
            <CardVeiculos titulo="Toro" imagem="http://localhost:8081/arquivosImagens/60b01f535af8e.jpg" class="cardItem" />
            <CardVeiculos titulo="gol g6" imagem="" class="cardItem" />
        </div>
    </div>
</template>

<script>

    import CardVeiculos from './CardVeiculos.vue';
    
    export default {
        name: 'Destaques',
        components:{
            CardVeiculos
        }
    }
</script>

<style>

    @font-face {
        font-family: NunitoExtrabold;
        src: url(~@/assets/fonts/nunito/Nunito-ExtraBold.ttf)
    }

    .section-content{

        padding-left: 7%;
        margin-top: 20px;
    }
    
    .titulo-content{
        font-family: NunitoExtrabold;
        font-size: 19pt;
        color: #0F2640;
    }

    #areaDadosCard{

        display: flex;
        margin-top: 10px;
    }

    .cardItem{

        margin-left: 20px;
    }
</style>