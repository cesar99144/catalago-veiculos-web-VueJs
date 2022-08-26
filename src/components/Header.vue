<template>
    <header>
        <div id="tituloArea">
            <h3>Catálogo veículos</h3>
        </div>
        <div id="areaPesquisa">
            <input id="entradaPesquisa" type="text" placeholder="Pesquisar veículo">
            <img src="@/assets/lupa.png" alt="" id="iconeLupa">
        </div>
        <div>
            Login
        </div>
    </header>
    <nav id="subMenu">
        <ul id="list">
            <li class="ativo">Destaques</li>
            <li>Carros</li>
            <li>Motos</li>
            <li>Filtragem</li>
            <li>Consultores</li>
        </ul>
    </nav>
</template>

<script>
    export default {
        name: 'Header'
    }
</script>

<style>

    @font-face {
        font-family: NunitoExtrabold;
        src: url(~@/assets/fonts/nunito/Nunito-ExtraBold.ttf)
    }

    header{
        background: #0F2640;
        display: flex;
        justify-content: space-between;
        padding: 15px;
        align-items: center;
        padding-left: 7%;
        padding-right: 10%;
    }

    #tituloArea{

        
    }

    #tituloArea > h3{

        color: #FFFF;
        font-family: NunitoExtrabold;
        font-size: 17pt;
    }

    #areaPesquisa{

        width: 40%;
        background: #FFFFFF;
        height: 40px;
        border-radius: 3px;
        margin-left: -5%;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding-left: 5px;
    }

    #entradaPesquisa{

        font-size: 13pt;
        width: 90%;
        border: none;
        outline: 0px;
    }

    #entradaPesquisa::placeholder{

        color: #0F2640;
        
    }

    #iconeLupa{

        width: 30px;
        height: 30px;
        padding: 10px;
    }

    #subMenu{

        background: #1E275A;
        padding: 20px;
        display: flex;
        justify-content: center;
    }

    #list{

        width: 60%;
        /* margin: auto; */
        text-align: center;

        
    }

    #list > li{
        display: inline;
        color: #FFFF;
        font-family: NunitoExtrabold;
        margin-left: 70px;
        cursor: pointer;
        font-size: 13pt;
    }

    .ativo{

        color: #E6DD3B !important;
        font-weight: bold;
    }

</style>