<template>
  <div class="million_box">
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
          questionText: "Di che colore è il cappello di Napoleone?",
          answersArray:[
            {
              answerText: "Giallo canarino",
              correct: false
            },
            {
              answerText: "Verde pisello",
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
          questionText: "Chi tra questi personaggi ha gli occhi neri",
          answersArray:[
            {
              answerText: "Tommaso Figlia",
              correct: true
            },
            {
              answerText: "Alfredo Lozano",
              correct: false
            },
            {
              answerText: "Mariapia Gianguzzi",
              correct: false
            },
            {
              answerText: "Raffaele Baldassarre",
              correct: false
            }
          ]
        },
        {
          questionText: "Quale, tra queste tecnologie, non è un linguaggio di programmazione",
          answersArray:[
            {
              answerText: "Javascript",
              correct: false
            },
            {
              answerText: "Html",
              correct: true
            },
            {
              answerText: "Php",
              correct: false
            },
            {
              answerText: "Java",
              correct: false
            }
          ]
        }
      ]
    }
  }

}
</script>

<style lang="scss">

</style>
