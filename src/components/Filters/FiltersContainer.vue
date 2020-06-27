<template>
             <!--EXcluir os Filtros  -->
    <div> 
        <h6> Excluir Questoes </h6>  
       
       <label class="label mt-5"   v-for="items in item" :key="items.text">
  <div class="toggle">
    <input class="toggle-state" type="checkbox" name="check" value="check" />
    <div class="indicator"></div>
  </div>

  <div   class="label-text">{{items.text}} </div>
</label>


             <!--Comentarios -->


      <h6> Comentarios </h6>  
   

   <label class="label mt-5"   v-for="index in comentarios" :key="index.text">
            <div 
                class="toggle">
                      <input 
                          class="toggle-state" 
                          type="checkbox" 
                          name="check" 
                          value="check" />
                        <div 
                          class="indicator">
                          </div>
            </div>

                    <div   
                    class="label-text">
                        {{index.text}} 
                    </div>
</label>


         <!--Os filtros serao renderizados aqui -->

        <v-card flat id="card" class="grey lighten-4 pa-5" > 
        Seus filtros aparecerão aqui...
        </v-card> 


<!--Botao para Filtrar Questoes  -->
<div id="filtrar"> 
        <v-btn text depressed class="mt-5" > Limpar </v-btn>
        <v-btn text depressed class="mt-5 ml-4" ><v-icon color="red" >mdi-plus</v-icon> Salvar Filtros </v-btn><br>

        <v-btn id="filtrarbtn" class="red mt-5 text-white" > Filtrar Questoes </v-btn>
</div>
    </div>
</template>

<script> 
export default { 
  data() {
    return ({ 
          item: [
              {text: "Anuladas"},
             { text: "Desatualizadas"},
          ],

          comentarios: 
[
{ text: "Comentários do professor"},
 {text: "Comentários dos alunos"},
 {text: "Meus comentários"}
          ]
      })
  }
}
</script>
<style scoped>

#card {
    height:60px;
    color: gray;
    display: flex;
}
@media only screen and (min-width: 950px) {
  #filtrar {
        position: relative;
        display: flex;
 

  }
  #filtrarbtn {
      margin-left: auto;
  }
}



.label {
  display: inline-flex;
  align-items: center;
  cursor: pointer;
  font-size: 14px;

}



.toggle {
  isolation: isolate;
  position: relative;
  height: 24px;
  width: 50px;
  border-radius: 15px;
  overflow: hidden;
background:#E0E0E0;
 margin-right: 10px;
    margin-left: 10px;
}



.toggle-state {
  display: none;
}

.indicator {
  height: 100%;
  width: 200%;
  background: white;
  z-index: 1;
  border-radius: 20px;
  border: 0.7px solid #F5F5F5;
  transform: translate3d(-75%, 0, 0);
  transition: transform 0.2s cubic-bezier(0.85, 0.05, 0.18, 1.35);

}

.toggle-state:checked ~ .indicator {
  background-color:#0091EA;
  transform: translate3d(20%, 0, 0);
}

@media only screen and (max-width: 950px) {
  #switcher {
      
  }
  .label {

        display: flex;
  flex-direction: row-reverse;
  justify-content: space-between;
  

  }
}




</style>