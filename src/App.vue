<template>
  <v-app>
   
 <Navigation/>

    <v-content>
     <Filters />
     <Questoes />
    </v-content>
  </v-app>
</template>

<script>
import Navigation from './components/Navigation';
import Filters from './components/Filters/Filters';
import Questoes from './components/Questoes/QuestoesFront';


export default {
  name: 'App',

  components: {
    Navigation,
    Filters,
    Questoes
  },

  data: () => ({
    //
  }),
};
</script>
