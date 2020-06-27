<template>
         <v-app   class=" grey lighten-4"> 
                  <div class="mr-12 ml-15 mt-10">
  
                        <simulado 
                        />
                                <Questoes 
                                />
                    </div>
            </v-app>
</template>


<script>
import simulado from './gerarSimulado';
import Questoes from './Questoes';
export default {
    components: {
        simulado,

        Questoes
    }
    
}
</script>
