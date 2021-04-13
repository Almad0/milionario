<template>
  <div class="question_box">
    <h3>Domanda</h3>
    <p>{{ questionsArray[0].questionText }}</p>
    <AnswerComponent/>
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
}
</script>
