<template >
<v-content >  
<div 
v-for="question in questions" :key="question.id">
      <v-layout col wrap row class="mt-10">
    <v-flex md1 pl-2 pr-2  sm1 xs1 class="grey lighten-3 pt-4 text-center"
            > 
   <p>{{question.id}}</p>
   </v-flex>
     <v-flex md3  sm3 xs3 class="grey lighten-3 text-center pt-4 " > 
   <p> Q1286982</p>
   </v-flex>

     <v-flex md4  sm4 xs6 class="grey lighten-3 text-center pt-4 " > 
<p> {{question.title}}</p>

   </v-flex>

    <v-flex md3  sm3 xs1 class="grey lighten-3 text-center pt-4 " > 
   </v-flex>

    <v-flex md1  sm1 xs1 class="grey lighten-3 text-center pt-4 " > 
   <v-icon small>mdi-plus-circle-outline</v-icon>
    </v-flex>






    <v-flex > 
   <h6>Ano:</h6><p>{{question.ano}}</p>
   </v-flex>
       <v-flex> 
   <h6>Banca:</h6><p>{{question.banca}} </p>
   </v-flex>

       <v-flex> 
    <h6>Órgão:</h6><p>{{question.orgao}}</p>

   </v-flex>

     <v-flex > 
    <h6>UF: </h6><p>{{question.uf}}  </p>
   </v-flex>

      <v-flex class="pt-2" >  
   <h6>Cargo:</h6> <p>{{question.cargo}} </p>
    </v-flex>


    


   </v-layout>  
   </div>
   </v-content>
</template>>

<script> 
import axios from 'axios'
export default { 
  data() {
    return {
      questions:[]
    }
  },
   created () {
    axios.get('http://localhost:3000/Question')
      .then(response => {
        this.questions = response.data
      })
      .catch(error => {
        console.log(error)
   

      })
    
  }
}

</script>
<style scoped>
h6, p {
    font-size:13px;

}

@media only screen and (max-width: 450px) {
  p {
   background-color: red;
  }
}



</style>