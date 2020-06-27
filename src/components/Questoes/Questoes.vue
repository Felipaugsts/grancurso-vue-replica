<template>
   <div class="mt-2">


<div class="mt-10" 
v-for="question of questions" :key="question">


<v-layout col wrap row class="mt-10">

              <!--Este e a ID  -->
       <v-flex 
            md1 pl-2 pr-2  sm1 xs1 
            class="pt-4 text-center"
            > 
                 <p>
                    {{question.id}}
                  </p>
       </v-flex>


            <!--ID da pergunta   -->
       <v-flex md3  sm3 xs3 
            class="text-center pt-4 " > 
                  <p> 
                      Q1286982  
                  </p>
        </v-flex>

              <!--Este o assunto  -->

      <v-flex md4  sm4 xs6 
            class="text-center pt-4 " > 

                    <p> 
                        {{question.title}}
                    </p>

       </v-flex>

            <v-flex md3  sm3 xs1 class="text-center pt-4 " > 
            </v-flex>

            <v-flex md1  sm1 xs1 class=" text-center pt-4 " > 
                  <v-icon small>
                    mdi-plus-circle-outline
                  </v-icon>
            </v-flex>



  <!--Informacoes adicionais da pergunta -->  

          <v-flex class="pl-2 pt-2" > 
                <h6>
                    Ano:
                </h6> 
                    <p>
                        {{question.ano}}
                    </p>
           </v-flex>

       <v-flex 
        class="pt-2" > 
              <h6>
                    Banca:
              </h6> 
                    <p>
                          {{question.banca}} 
                    </p>
         </v-flex>

         <v-flex class="pt-2" > 
                <h6>
                  Órgão:
                  </h6>
                      <p>
                        {{question.orgao}}
                      </p>
          </v-flex>

         <v-flex class="pt-2" > 
               <h6>
               UF: 
               </h6>
                     <p>
                     {{question.uf}}  
                     </p>
          </v-flex>

          <v-flex class="pt-2" >  
                <h6>
                  Cargo:
                </h6> 
                <p>
                  {{question.cargo}} 
                </p>
            </v-flex>

   </v-layout>  




                <!--  PERGUNTA -->
  

    <p  
        class="mt-8">
          {{question.questao}}
      </p>

                    <!--  Opcoes de resposta  -->
            <v-card 
                flat 
                class="grey lighten-4 d-flex text-center"
                      v-for="resposta of respostas" 
                      :key="resposta"
                      >


                        <v-card
                        class="grey lighten-4 "
                        flat 
                        height="30"
                        width="40"
                        tile 
                        >

                        <!--  botao para descartar pergunta -->
                                  <v-btn 
                                      color="blue" 
                                      icon
                                      >
                                            <v-icon 
                                                    medium 
                                                    class="mb-2"
                                                    >
                                                    mdi-window-minimize
                                              </v-icon>
                                    </v-btn>
                        </v-card>

              <v-card
                    class="grey lighten-4 "
                    flat 
                    height="30"
                    width="40"
                    tile >
                    <v-btn 
                        color="blue" 
                        id="btn"  
                        outlined x-small icon>
                        {{resposta.button}}
                    </v-btn>
                </v-card>


        <v-card
              class="grey lighten-4 "
              flat 
              height="30"
              width=""
              tile
              >
                  {{resposta.option}}
      </v-card>
</v-card>


                  <!--  Botao para responder -->


<v-btn class="blue accent-4 mt-12 pa-5 text-white"> Responder </v-btn>


</div>

 </div>
</template>

<script>
import axios from 'axios';
export default {
    data: function () {
      return  ({
      respostas: [
       
      ],
  
      questions: []
    
}

    )
    },
    created () {
    axios.get('http://localhost:3000/Question')
      .then(response => {
        this.questions = response.data
      })
      .catch(error => {
        console.log(error)

   

      }),

        axios.get(' http://localhost:3000/respostas')
      .then(response => {
        this.respostas = response.data
      })

    
  }
   
   
}
</script>

<style scoped>
p {
    font-size: 13px;
}
</style>>
