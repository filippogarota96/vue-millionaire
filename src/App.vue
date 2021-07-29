<template>
 
    <div id="app">
      <div id="nav">
      
        <contenitore></contenitore>
        <domanda :color="'nero'"></domanda>
        <risposta></risposta>
      
      
      <div class="row-question">

        
      </div>
      
    </div>
  
      
    
    <router-view />
  </div>
</template>

<script>
import Contenitore from "@/components/Contenitore.vue"
import Domanda from "@/components/Domanda.vue"
import Risposta from "@/components/Risposta.vue"


export default {
  name: 'App',
  components: {
    'contenitore': Contenitore,
    'domanda': Domanda,
    'risposta': Risposta
  },
  data() {
    return {
      questions: [
        {
          question: "In che anno è stata scoperta l'America?",
          answ1: "1321",
          answ2: "1492",
          answ3: "1540",
          answ4: "1200"
        },

        {
          question: "Come mi chiamo?",
          answ1: "Giacomo",
          answ2: "Daniele",
          answ3: "Filippo",
          answ4: "Carlo"
        },

        {
          question: "Ricetta della cabonara?",
          answ1: "pesce, aglio, prezzemolo",
          answ2: "salsiccia, pecorino, miele",
          answ3: "uova, guanciale, pepe",
          answ4: "zucchine, uova, caviale"
        }

      
      ]
    
    }
  }
}








</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}



</style>
