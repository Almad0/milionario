<template>
  <div class="question_box">
    <div class="Q_box">
      <div class="left_tri"></div>
      <p>{{ questionsArray[this.rand].questionText }}</p>
      <div class="right_tri"></div>
    </div>
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
    // console.log(this.questionsArray[this.rand].answersArray)
  }

}


</script>

<style lang="scss">
.question_box{
  .Q_box{
    width: 60%;
    margin: auto;
    padding: 30px;
    display: flex;
    justify-content: center;
    align-items: center;
    p{
      padding: 10px 100px;
      color: white;
      text-align: center;
      border: 2px solid white;
    }
  }
}
</style>
