<template>
    <div class="section-content">
        <h3 class="titulo-content">Veículos em destaque</h3>

        <div id="areaDadosCard">
            <div class="cardItem"  v-for="veiculo in listaVeiculos" :key="veiculo.idVeiculo">
                <CardVeiculos 
                    :titulo="veiculo.tituloAnuncio"
                    :imagem="veiculo.primeiraImagem"
                    :marca="veiculo.marca"
                    :modelo="veiculo.modelo"
                    :ano="veiculo.ano"
                    :preco="veiculo.preco"
                />
            </div>
        </div>
    </div>
</template>

<script>

    import CardVeiculos from './CardVeiculos.vue';
    
    export default {
        name: 'Destaques',
        components:{
            CardVeiculos
        },
        data(){
            return{
                listaVeiculos: []
            }
        },
        methods:{

            async getVeiculosDestaques(){

                const requisicao = await fetch('http://localhost:4000/destaques');
                const data = await requisicao.json();

                this.listaVeiculos = data;

                console.log(this.listaVeiculos)
            }
        },
        mounted(){

            this.getVeiculosDestaques();
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
        grid-row: 1;
        margin-top: 10px;
    }

    .cardItem{

        margin-left: 20px;
        width: 18%;
        /* border: 1px solid; */
    }
</style>