<template>

<div > 
        <h6 class="mt-3"> 
            Minhas Questōes 
        </h6>  
    <v-layout row wrap justify-start>  
        <v-flex md5 lg5 sm12 xs12>
                             
                  
        </v-flex>
    </v-layout>

    <div class="switcher"> 
    
     <label class="label mt-5"   v-for="items in item" :key="items.text">
  <div class="toggle">
    <input class="toggle-state" type="checkbox" name="check" value="check" />
    <div class="indicator"></div>
  </div>

  <div   class="label-text">{{items.text}} </div>
</label>

    </div>

 </div>

</template>

<script>
export default {
  data() {
      return ({ 
          item: [
              {text: "Todas"},
             { text: "Ja resolvi"},
             { text: "Nao resolvi"},
           {   text: "Acertei" },
             { text: "Errei"}
              
          ]
      })
  }
}
</script>

<style scoped>
#questoes {
    padding: 50px;
}

.switcher {
    background-color: red;
  font-weight: 300;
  background-color: white;
    
}


.label {
  display: inline-flex;
  align-items: center;
  cursor: pointer;

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
  border-radius: 15px;
  border: 0.4px solid gray;
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