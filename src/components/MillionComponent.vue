<template>
  <div class="million_box">
    <h2>Chi vuol'essere milionario? Tua sorella? </h2>
    <QuestionComponent v-bind:questionsArray="questionsArray"/>
  </div>
</template>

<script>
import QuestionComponent from "./QuestionComponent"


export default {
  name: "MillionComponent",
  components: {
    QuestionComponent
  },
  data() {
    return {
      questionsArray: [
        {
          questionText: "Di che colore è la cappella di Napoleone?",
          answersArray:[
            {
              answerText: "Giallo canarino",
              correct: false
            },
            {
              answerText: "Verde Pisello",
              correct: true
            },
            {
              answerText: "Indaco spaziale",
              correct: false
            },
            {
              answerText: "Terra di Siena",
              correct: false
            }
          ]
        },
        {
          questionText: "Chi tra questi è un truffatore di merda?",
          answersArray:[
            {
              answerText: "Lupin 3",
              correct: false
            },
            {
              answerText: "Silvio Berlusconi",
              correct: false
            },
            {
              answerText: "Maria Pia Gianguzzi",
              correct: false
            },
            {
              answerText: "Fabio Pacifici",
              correct: true
            }
          ]
        }
      ]
    }
  }

}
</script>
