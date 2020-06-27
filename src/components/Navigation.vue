<template>
  <div id="navbar"> 
  <div id="small" class="text-center mt-4">

<v-icon id="menu"> mdi-menu </v-icon>

<img  id="icon" src="@/assets/nav.png" />

<v-btn icon >
      <v-icon id="icon">mdi-account-circle</v-icon>
   </v-btn>
</div>
<div id="large" > 
<img id="img" src="@/assets/nav.png" />
<ul> 
<li v-for=" items in navItem" :key="items"> {{items.text}}</li>

</ul>
<v-btn text id="avatar">
      <v-icon large>mdi-account-circle</v-icon> Olá, Felipe  
    </v-btn>
</div>


  </div>
</template>
<script>
export default { 
  data() {
    return{ 
      navItem: [ 
        
          {text: "Provas"},
          {text: "Questoes para Concursos"},
          {text: "Questoes para OAB"},
          {text: "Assuntos Frequentes"},
        
      ]
    }
  }
}
</script>

<style scoped>

#navbar { 
  background-color: white;
  width: 100%;
  height: 60px;
  z-index: 1;
  position: fixed;

}
img { 
  height: 30px;  
}
#large{ 
  display: flex;
  margin-top: 15px;
}
#avatar {
  margin-left: 7%; 
  margin-right: 20px;

}
ul li { 

  display: inline;
  padding: 20px;
  list-style: none;
font-weight: bold;
cursor: pointer;
}

#img { 
  margin: 0px 10px 0px 90px;
}

#small{
  display:none;
}
#icon {

margin-left: 20%;
margin-right: 20%;

}
#menu {

}

@media only screen and (max-width: 1250px) {
    #avatar {
     margin-left: 1%; 
  margin-right: 40px;
  }
  ul li { 
    font-size: 14px;
  }
}

@media only screen and (max-width: 1130px) {
    #large {
 display: none;
  }
#small {
      display: flex;
      justify-content: center;
  }
}
</style>
