<template>
  <div class="question_box">
    <h3>Domanda</h3>
    <p>{{ questionsArray[this.rand].questionText }}</p>
    <AnswerComponent v-bind:currentQuestion="currentQuestion"/>
  </div>
</template>

<script>
import AnswerComponent from "./AnswerComponent";

export default {
  name: "QuestionComponent",
  props: {
    questionsArray: Array
  },
  components: {
    AnswerComponent
  },

  data() {
    return {
      rand: 0,
      currentQuestion: []
    }
  },

  created() {
    this.rand = Math.floor(Math.random() * this.questionsArray.length);
    this.currentQuestion = this.questionsArray[this.rand].answersArray;
    console.log(this.questionsArray[this.rand].answersArray)
  }

}


</script>
