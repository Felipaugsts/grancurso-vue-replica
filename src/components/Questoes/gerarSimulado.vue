<template>
    <content id="simulado"> 
    <ul>
                 <li>
                    A+
                </li>
                <li>
                     A-
                </li>
                            <li>
                                    <v-icon 
                                            color="black">
                                                    mdi-brightness-2
                                    </v-icon>
                            </li>
     </ul> 

      <div id="gerar"> 
                <v-btn 
                    class="indigo accent-4 text-white" > 
                            <v-icon 
                                small color="white">
                                        mdi-plus
                            </v-icon> 
                        Gerar Simulado 
                </v-btn>
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