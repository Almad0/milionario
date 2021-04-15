<template>
  <div class="million_box">
    <QuestionComponent v-bind:questionsArray="questionsArray" v-if="questionsArray"/>
  </div>
</template>

<script>
import QuestionComponent from "./QuestionComponent";
import axios from 'axios';
const ax = axios.create({
  baseURL: "http://localhost:8080/",
});


export default {
  name: "MillionComponent",
  components: {
    QuestionComponent
  },
  data() {
    return {
      questionsArray: null
    }
  },
  mounted() {
    let url = "data.json";
    ax.get(url)
      .then((response) => {
        this.questionsArray = response.data;
        console.log(response.data);
      })
  }
}
</script>

<style lang="scss">

</style>
