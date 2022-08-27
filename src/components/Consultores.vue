<template>
    <div class="content-consultores">
       <div class="topo-consultores">
          
       </div>
       <div class="dadosConsultores">
            <div>
                <img id="imagemConsultores" src="@/assets/atendimento-ao-cliente.png" alt="">
            </div>
            <div id="formContato">
                <h3>Preencha os dados e um dos nossos consultores entrará em contato com você</h3>

                <form action="" id="contato">
                    <input type="text" placeholder="Nome">
                    <input type="text" placeholder="Email">
                    <input type="text" placeholder="Celular">
                    <textarea name="" id="" cols="30" rows="2" placeholder="Modelo de interresse"></textarea><br>
                    <button id="botaoEnviarForm">Enviar dados</button>
                </form>
            </div>
       </div>
    </div>
</template>

<script>
    export default{
        name: 'Consultores'
    }
</script>

<style>

    @font-face {
        font-family: NunitoExtrabold;
        src: url(~@/assets/fonts/nunito/Nunito-ExtraBold.ttf)
    }

    .content-consultores{

        border: 1px solid;
        padding: 2%;
        padding-left: 5%;
        background: #0F2640;
        margin-top: 3%;
    }

    .dadosConsultores{

        display: flex;
    }

    #imagemConsultores{

        width: 80%;
        margin-top: 50px;
    }

    #formContato{

        margin-top: 20px;
    }

    #formContato > h3{

        font-family: NunitoExtrabold;
        font-size: 19pt;
        color: white;
        text-align: center;
    }

    #contato{

        margin-top: 20px;
        align-items: center;
        text-align: center;
    }

    #contato > input{

        width: 70%;
        padding: 10px;
        border: none;
        border-radius: 3px;
        outline: 0px;
        margin-top: 15px;
    }

    #contato > textarea{

        width: 70%;
        padding: 10px;
        border: none;
        border-radius: 3px;
        outline: 0px;
        margin-top: 15px;
    }

    #botaoEnviarForm{

        width: 73%;
        margin-top: 20px;
        background: teal;
        color: white;
        padding: 10px;
        border: none;
        border-radius: 3px;
        cursor: pointer;
        font-family: NunitoExtrabold;
    }

</style>