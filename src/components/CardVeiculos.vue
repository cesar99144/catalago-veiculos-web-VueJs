<template>
    <div class="card">
        <div class="imagemCard">
            <img :src="'http://localhost:4000/imagensVeiculos/'+imagem" alt=""/>
        </div>
        <div class="tituloCard">
            <h3>{{titulo}}</h3>
        </div>
        <div class="descricaoCard">
            <label class="textoDescricao">Marca: <span class="descricaoDestaque">{{marca}}</span></label><br>
            <label class="textoDescricao">Modelo: <span class="descricaoDestaque">{{modelo}}</span></label><br>
            <label class="textoDescricao">Ano: <span class="descricaoDestaque">{{ano}}</span></label><br>
            <label class="textoDescricao">Preço: <span class="descricaoDestaque">R$ {{parseFloat(preco).toFixed(3)}}</span></label>
        </div>
        <div class="botoesCard">
            <button class="botaoInfo">Mais informações</button>
        </div>
    </div>
</template>

<script>
    export default{
        name: 'CardVeiculos',
        data(){
            return{
                nomeVeiculo: 'teste'
            }
        },
        props:{
            titulo: String,
            imagem: String,
            marca: String,
            modelo: String,
            ano: String,
            preco: Number
        }
    }
</script>

<style>

    @font-face {
        font-family: NunitoExtrabold;
        src: url(~@/assets/fonts/nunito/Nunito-ExtraBold.ttf)
    }
    .card{

        background: #FFFFFF;
        margin-top: 10px;
        height: 350px;
        border: none;
        /* width: 16%; */
        width: 90%;
        /* box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px; */
        box-shadow: rgba(50, 50, 93, 0.25) 0px 2px 5px -1px, rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;
        padding: 10px;
    }

    .imagemCard{

        width: 100%;
        height: 40%;
    }

    .imagemCard > img{

        width: 100%;
        height: 100%;
        object-fit: cover;
    }

    .tituloCard{

        margin-top: 10px;
        padding-left: 11px;
    }

    .tituloCard > h3{

        font-family: NunitoExtrabold;

    }

    .descricaoCard{

        height: 30%;
        margin-top: 10px;
        padding-left: 11px;
    }

    .botoesCard{

        margin-top: 10px;
        height: 12%;
    }

    .botaoInfo{

        background: #0F2640;
        width: 100%;
        color: white;
        padding: 10px;
        border: none;
        border-radius: 3px;
        cursor: pointer;
        font-family: NunitoExtrabold;
    }

    .descricaoDestaque{

        font-weight: bold;
        color: #0F2640;
    }

    .textoDescricao{

        font-size: 11pt;
    }

</style>