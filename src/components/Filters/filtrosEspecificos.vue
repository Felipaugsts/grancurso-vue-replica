<template>
<div>
                        <!--Selecione por Disciplina e Assuntos  -->
  <v-layout row wrap id="filter"  > 
              <v-flex md6 sm6 xs6 pr-2 pl2 > 
                <v-select
                     
                      :items="assunto"
                      label="Selecione por Disciplina e Assuntos"
                      multiple
                      
                      
                      >
                          <template v-slot:selection="{ item, index }">
                              <v-chip v-if="index === 0">
                                      <span>
                                              {{ item }}
                                      </span>
                                </v-chip>           
                          </template>
                </v-select>
            </v-flex>
   


            <v-flex md3  sm12 xs12 pr-2 pl2> 
                <v-select
                
                          :items="nivel"
                          label="Nivel"
                          multiple
                            >
                         <template v-slot:selection="{ item, index }">
                              <v-chip v-if="index === 0">
                                     <span>{{ item }}</span>
                              </v-chip>
                       </template>
                  </v-select>
             </v-flex>
  
            <v-flex md3  sm12 xs12 pr-2 pl2> 
                <v-select
                        
                          :items="bancas"
                          label="Banca"
                          multiple
                            >
                         <template v-slot:selection="{ item, index }">
                              <v-chip v-if="index === 0">
                                     <span>{{ item }}</span>
                              </v-chip>
                       </template>
                  </v-select>
             </v-flex>



             <v-flex md3  sm12 xs12 pr-2 pl2> 
                <v-select
                         label="Orgao"
                          :items="orgao"
                          multiple
                            >
                         <template v-slot:selection="{ item, index }">
                              <v-chip v-if="index === 0">
                                     <span>{{ item }}</span>
                              </v-chip>
                       </template>
                  </v-select>
             </v-flex>



             <v-flex md3  sm12 xs12 pr-2 pl2> 
                <v-select
                   
                          :items="ano"
                          label="Ano"
                          multiple
                            >
                         <template v-slot:selection="{ item, index }">
                              <v-chip v-if="index === 0">
                                     <span>{{ item }}</span>
                              </v-chip>
                       </template>
                  </v-select>
             </v-flex>

           <v-flex md3  sm12 xs12 pr-2 pl2> 
                <v-select
                          :items="items"
                          label="Cargo"
                          multiple
                            >
                         <template v-slot:selection="{ item, index }">
                              <v-chip v-if="index === 0">
                                     <span>{{ item }}</span>
                              </v-chip>
                       </template>
                  </v-select>
             </v-flex>

            <v-flex md3  sm12 xs12 pr-2 pl2> 
                <v-select
             
                          :items="bancas"
                          label="Tipo de Questao"
                          multiple
                            >
                         <template v-slot:selection="{ bancas, index }">
                              <v-chip v-if="index === 0">
                                     <span  >{{ bancas }}</span>
                                   
                              </v-chip>
                       </template>
                  </v-select>
             </v-flex>
    </v-layout>
</div>
</template>
<script>

  export default {
     data: () => ({
      assunto: ['Administração Financeira e Orçamentária - AFO', 'Administração Geral','Biologia','Ciência Política'],
      nivel: ['junior','senior'],
      items: ['Filters here', 'filter one' , 'filter two'],
      bancas: ['Academia de Polícia Civil de Minas Gerais ', 'Associação Catarinense das Fundações Educacionais' , 'Consultoria e Assessoria Técnica e Estados e Municípios', 'Informática' ],
       orgao: ['Administração dos Portos de Paranaguá e Antonina ', 'Advocacia Geral do Estado de Minas Gerais - AGE - MG' , 'Advocacia-Geral da União - AGU - BR', 'Agência Brasileira de Inteligência - ABIN - BR' ],
        ano: ['2015','2016','2017','2018','2019']

    
    })
    

  }
</script>

<style scoped>
#filter {
     opacity: 0.5;
}
</style>>




