<template>
 
    <div id="app">
      <div id="nav">
      
      <contenitore></contenitore>
      <domanda :qst="questions[radomIndex].question"></domanda>
      <div class="answer-container">
        <risposta v-for="item in questions[radomIndex].answers" :key="item.id" class="answer" :answ=" item.text" :class="correct ? check(item) : '' " v-on:choose-answer="select"></risposta>
      </div>
      
    </div>
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
  data: function() {
    return {
      radomIndex: 0,
      correct: false,
      questions: [
        {
          question: "In che anno è stata scoperta l'America?",
          answers: [
            {text: '1219', },
            {text: '1492', correct: true},
            {text: '1569', },
            {text: '1321', },
             
          ]
        },
        {
          question: "Come mi chiamo?",
          answers: [
            {text: 'Daniele', },
            {text: 'Filippo', correct: true},
            {text: 'Giacomo', },
            {text: 'Carlo', }, 
          ]
        },
        {
        question: "Ricetta della cabonara?",
         answers: [
            {text: 'tonno, pomodoro, sedano', },
            {text: 'cipolle, bacon, panna', },
            {text: 'uova, pepe, guanciale', correct: true},
            {text: 'basilico, pinoli', }, 
          ]
        }
      ]
    }
  },
  mounted: function() {
    this.radomIndex = Math.floor(Math.random() * this.questions.length)
  },
  methods: {
    select(){
      this.correct = true;
    },

    check(answ) {
      if (answ.correct == true) {
        return 'correct';
      } else {
        return 'wrong';
      }
    }
  }
}



</script>

<style lang="scss" scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  background-color: #11093A;
  text-align: center;
  
  .answer-container {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      width: 60%;
      margin: 0 auto;
  
  }
  .answer {
    margin: 45px;
   
  }

  .correct {
    background-color: green;
  }

  .wrong {
    background-color: red;
  }
  
}


</style>
