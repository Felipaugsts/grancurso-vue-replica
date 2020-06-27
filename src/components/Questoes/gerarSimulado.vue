<template>
    <content id="simulado"> 
    <ul>
    <li>A+</li>
    <li>A-</li>
    <li><v-icon color="black">mdi-brightness-3</v-icon></li>
     </ul> 

      <div id="gerar"> 
          <v-btn class="indigo accent-4 text-white" > <v-icon small color="white">mdi-plus</v-icon> Gerar Simulado </v-btn>
      </div>

    </content>
</template>
<style scoped>

li {
    list-style: none;
    display: inline;
    margin-right: 20px;
    cursor: pointer;
}

#gerar {
  
   
    margin-right: 10px;
}
@media only screen and (min-width: 950px) {
  #simulado {
        position: relative;
        display: flex;
  }
  #gerar {
     margin-left: auto;
  }
}

</style>>