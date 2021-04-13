<template>
  <div class="answer_box">
    <h4>Risposte</h4>
    <p>{{ currentQuestion[0].answerText }}</p>
    <p>{{ currentQuestion[1].answerText }}</p>
    <p>{{ currentQuestion[2].answerText }}</p>
    <p>{{ currentQuestion[3].answerText }}</p>

  </div>
</template>

<script>
export default {
  name: "AnswerComponent",
  props: {
    currentQuestion: Array
  },
  mounted() {
    console.log(this.currentQuestion)
  }
}
</script>
