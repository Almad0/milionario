<template>
  <div class="answer_box">
    <div class="A_box">
      <p v-for="questions in currentQuestion">{{ questions.answerText }}</p>
    </div>

<!--    <p>{{ currentQuestion[0].answerText }}</p>
    <p>{{ currentQuestion[1].answerText }}</p>
    <p>{{ currentQuestion[2].answerText }}</p>
    <p>{{ currentQuestion[3].answerText }}</p>-->

  </div>
</template>

<script>
export default {
  name: "AnswerComponent",
  props: {
    currentQuestion: Array
  },
  mounted() {
    // console.log(this.currentQuestion)
  }
}
</script>

<style lang="scss">
  .A_box{
    width: 70%;
    margin: auto;
    padding: 30px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    align-items: center;
    color: white;
    p{
      width: calc(40% - 20px);
      margin: 20px;
      padding: 10px 0;
      color: white;
      text-align: center;
      border: 2px solid white;
    }
  }
</style>
