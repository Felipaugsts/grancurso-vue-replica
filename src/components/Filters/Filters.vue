
<template>
                       <!-- Pagina que esta sendo Renderizada no App.js   -->
    <v-app>

   
  
        <div id="content"> 
        <ul> 
        <li> 
        Home /
        Questoes /
        Concursos Publicos 
        </li>
        
        </ul>
        <p> Questoes para Concursos</p>
             </div>
             <v-content class="mr-15 ml-15 mb-5">  

                <!-- Este sao os Filtros   -->
  

        <h6 
            class="mt-2" >Filtros
        </h6> 
    
    <v-layout row wrap justify-end>  
        <v-flex md3 lg3 pl-1>
                 <div id="filter" class="custom-select">
                    <option selected>
                             Filtros Salvos
                     </option>
                </div>
        </v-flex>
    </v-layout>


        <!-- Esta sao as Questoes  -->
             <questions/>

         <!-- Filtros especificos  -->

            <filtrosEspecificos/>

     <!-- Esta sao as Questoes  -->

     <FiltersContainer/>
  


    </v-content>





    </v-app>
</template>

<script> 
import questions from './filtroQuestoes'
import filtrosEspecificos from './filtrosEspecificos'
import FiltersContainer from './FiltersContainer'
export default { 

    components: {
                questions,
                filtrosEspecificos,
                FiltersContainer
    }
}
</script>

<style scoped>

#content { 
    height: 160px;
    width: 100%;
    margin-top: 60px;
    background-color:#0A2033;
    color: white;
}

#questoes {
    height: 200px;
}

ul li {
    list-style: none;
    margin-top: 45px;
    margin-bottom: 0px;
    font-size: 11px;
    margin-left: 3%;


}
p { 
    font-size: 28px;
    margin-left: 6%;
}

#filter{
    opacity:0.5;
    cursor:pointer;
}

</style>