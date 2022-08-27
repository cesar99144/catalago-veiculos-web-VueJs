<template>
    <div id="carros" class="section-content-veiculos">
        <div class="areaTopo-veiculos">
            <div class="logo-tituloCarros">
                <img src="@/assets/Car.png" alt="">
                <h3 class="titulo-content-veiculos">Carros</h3>
            </div>
            <div class="">
                
            </div>
        </div>
        <div id="areaDadosVeiculos">
            <div id="areaDadosCard-veiculos">
                <div class="areaFiltroVeiculos">
                    <FiltrarDados />
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
    import FiltrarDados from './FiltrarDados.vue';
    
    export default {
        name: 'Carros',
        components:{
            CardVeiculos,
            FiltrarDados
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

    .section-content-veiculos{

        /* padding-left: 7%; */
        margin-top: 20px;
    }

    .areaTopo{

       
    }

    .areaTopo-veiculos{

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
    
    .titulo-content-veiculos{
        font-family: NunitoExtrabold;
        font-size: 19pt;
        /* color: #0F2640; */
        color: #FFFFFF;
    }

    #areaDadosVeiculos{

        display: flex;
        padding-left: 40px;
    }

    #areaDadosCard-veiculos{

        display: flex;
        margin-top: 10px;
        width: 100%;
        
    }

    .areaFiltroVeiculos{

        width: 20%;
        background: #FFFFFF;
        padding: 10px;
        margin-top: 20px;
        height: 60%;
    }

    .cardAreaVeiculo{
        display:grid;
        /* grid-template-columns:repeat(4, auto); */
        grid-template-columns:repeat(auto-fit, minmax(25%, 1fr));
        width: 100%;
        margin-left: 10px;
        /* width: 80%; */
    }

    .cardVeiculolist{

        margin-left: 20px;
        margin-top: 10px;
        /* width: 120px; */
    }
</style>