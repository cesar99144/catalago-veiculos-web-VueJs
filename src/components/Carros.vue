<template>
    <div id="carros" class="section-content-carros">
        <div class="areaTopo-carros">
            <div class="logo-tituloCarros">
                <img src="@/assets/Car.png" alt="">
                <h3 class="titulo-content-carros">Carros</h3>
            </div>
            <div class="">
                aplicar filtros
            </div>
        </div>
        <div id="areaDadosVeiculos">
            <div id="areaDadosCard-carros">
                <div class="areaFiltroVeiculos">
                    Filtros
                </div>
                <div class="cardAreaVeiculo">
                    <div class="cardVeiculolist" v-for="veiculo in listaVeiculos" :key="veiculo.idVeiculo">
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
        </div>
        
    </div>
</template>

<script>

    import CardVeiculos from './CardVeiculos.vue';
    
    export default {
        name: 'Carros',
        components:{
            CardVeiculos
        },
        data(){
            return{
                listaVeiculos: []
            }
        },
        methods:{

            async getVeiculosCarros(){

                const requisicao = await fetch('http://localhost:4000/carros');
                const data = await requisicao.json();

                this.listaVeiculos = data;

                console.log(this.listaVeiculos)
            }
        },
        mounted(){

            this.getVeiculosCarros();
        }
    }
</script>

<style>

    @font-face {
        font-family: NunitoExtrabold;
        src: url(~@/assets/fonts/nunito/Nunito-ExtraBold.ttf)
    }

    .section-content-carros{

        /* padding-left: 7%; */
        margin-top: 20px;
    }

    .areaTopo{

        border: 1px solid;
    }

    .areaTopo-carros{

        background: #0F2640;
        padding: 15px;
        padding-left: 3%;
        padding-right: 7%;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .logo-tituloCarros{

        display: flex;
        border: 1px solid;
        width: 30%;
        align-items: center;
    }

    .logo-tituloCarros > img{

        width: 60px;
        height: 60px;
    }

    .logo-tituloCarros > h3{

        margin-left: 10px;
    }
    
    .titulo-content-carros{
        font-family: NunitoExtrabold;
        font-size: 19pt;
        /* color: #0F2640; */
        color: #FFFFFF;
    }

    #areaDadosVeiculos{

        display: flex;
        padding-left: 40px;
    }

    #areaDadosCard-carros{

        display: flex;
        margin-top: 10px;
        width: 100%;
        border: 1px solid;
        
    }

    .areaFiltroVeiculos{

        border: 1px solid;
        width: 15%;
    }

    .cardAreaVeiculo{
        display:grid;
        /* grid-template-columns:repeat(4, auto); */
        grid-template-columns:repeat(auto-fit, minmax(25%, 1fr));
        width: 100%;
        border: 1px solid;
        margin-left: 40px;
        /* width: 80%; */
    }

    .cardVeiculolist{

        margin-left: 20px;
        margin-top: 10px;
        /* width: 120px; */
    }
</style>