<template>
    <div class="tituloFiltros">
        <h4>Filtrar dados</h4>
        <div class="areaDadosBusca">
            <div class="containerEntradaDados">
                <label for="">Pesquisar</label><br>
                <input type="text" placeholder="Digita um valor">
            </div>
            <div class="containerEntradaDados">
                <label for="">Marcas</label><br>
                <select name="" id="">
                    <option value=""></option>
                </select>
            </div>
            <div class="containerEntradaDados">
                <label for="">Modelos</label><br>
                <select name="" id="">
                    <option value=""></option>
                </select>
            </div>
            <div class="containerEntradaDados">
                <label for="">Ano</label><br>
                <select name="" id="">
                    <option value=""></option>
                </select>
            </div>
            <div class="containerEntradaDados">
                <label for="">Faixa preço</label><br>
                <select name="" id="">
                    <option value=""></option>
                </select>
            </div>
            <div class="containerBotaoPesquisar">
                <button>Pesquisar</button>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'FiltrarDados'
    }
</script>

<style>

    @font-face {
        font-family: NunitoExtrabold;
        src: url(~@/assets/fonts/nunito/Nunito-ExtraBold.ttf)
    }

    .tituloFiltros{
        text-align: center;
        margin-top: 10px;
    }

    .tituloFiltros > h4{
        font-family: NunitoExtrabold;
    }

    .areaDadosBusca{

        margin-top: 10px;

    }

    .containerEntradaDados{

        text-align: left;
        margin-top: 10px;
    }

    .containerEntradaDados > label{

        font-family: NunitoExtrabold;
    }

    .containerEntradaDados > input{

        width: 90%;
        background: #5d5f66;
        border: none;
        outline: none;
        padding: 10px;
        color: #eeefef;
        font-weight: bold;
    }

    .containerEntradaDados > input::placeholder{

        color: #eeefef;
    }

    .containerEntradaDados > select{

        width: 100%;
        background: #5d5f66;
        border: none;
        outline: none;
        padding: 10px;
        color: #eeefef;
        font-weight: bold;
    }

    .containerBotaoPesquisar{

        margin-top: 20px;
    }

    .containerBotaoPesquisar > button{

        background: #0F2640;
        width: 100%;
        color: white;
        padding: 10px;
        border: none;
        border-radius: 3px;
        cursor: pointer;
        font-family: NunitoExtrabold;
    }

</style>