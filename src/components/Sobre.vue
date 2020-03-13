<template>
    <div> 
        <div class="sobre" id="sobre">
            <div>
                <h2> Sobre nós </h2>
                <div id="content">
                    <div id="textoSobre">
                        <p> Somos um projeto desenvolvido pela Casa Magalhães, com o objetivo de lapidar jovens devs para o mercado de trabalho
                    e desenvolver projetos de alta qualidade. <br> <br>
                    Contamos com times ágeis e autogerenciados de desenvolvimento web e ciência de dados, prontos para entregarem as melhores
                    soluções, abastecidos com um bom café.
                    </p>
                    </div>
                     

                         <div id="imgDevAcademy">
                            <img  src="../assets/ambienteDevAcademy.jpeg" alt="DevAcademy" style=" width: calc(100% - 32px)">
                        </div>
                    </div>
               
                
                
            </div>
        </div>
    </div>
</template>

<style lang="stylus" scoped>
    h2 {
        margin: 20px;
        color: #fff;
        font-size: 35px;
    }

    .sobre {
        padding: 0 5% 64px 5%;
        margin-top: 800px;
    }

    p {
        font-size: 25px;
        color: #fff;
    }

    #imgDevAcademy {
        margin: 20px;
        height: 750px;
        float: left;
        width: calc(50% - 32px);
        
    }

    #textoSobre {
        float: left;
        width: calc(50% - 32px);
        
    }

    #content {
        margin: 20px;
        
    }
    
</style>