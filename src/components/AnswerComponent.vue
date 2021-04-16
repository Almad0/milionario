<template>
  <div class="answer_box">
    <div class="A_box">
      <p  @click="correct_or_wrong (index)" v-for="(questions, index) in currentQuestion" :id="index" >{{ questions.answerText }}</p>
    </div>

  </div>
</template>

<script>
export default {
  name: "AnswerComponent",
  props: {
    currentQuestion: Array
  },
  data(){
    return{
      correct: 0
    }
  },
  methods:{
    correct_or_wrong(e){
      console.log(e);
      if (this.currentQuestion[e].correct){
        document.getElementById(e).style.backgroundColor= "green"
      } else{
        document.getElementById(e).style.backgroundColor= "red";
        for (let i=0; i<4; i++) {
          if (this.currentQuestion[i].correct) {
            document.getElementById(i).style.backgroundColor = "green";
            break;
          }
        }
      }
      console.log(this.currentQuestion[e].correct)
    }
  },
  mounted() {
    console.log(this.currentQuestion)
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
      padding: 10px;
      margin: 20px;
      color: white;
      text-align: center;
      border: 2px solid white;
    }
    .red{
      background-color: darkred;
    }
    .green{
      background-color: darkgreen;
    }
  }
</style>
