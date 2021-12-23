
<template>
  <h1>Just Tests</h1>

  <div id="watch-example">
  <p>
    Ask a yes/no question:
    <input v-model="question" />
  </p>
  <p>{{ answer }}</p>
</div>
</template>

<!-- <script src="https://cdn.jsdelivr.net/npm/axios@0.12.0/dist/axios.min.js"></script> -->
<script>
export default {
   data() {
      return {
        question: '',
        answer: 'Questions usually contain a question mark. ;-)'
      }
    },
    watch: {
      // whenever question changes, this function will run
      question(newQuestion, oldQuestion) {
          console.log(oldQuestion);
        if (newQuestion.indexOf('?') > -1) {
          this.getAnswer()
        }
      }
    },
    methods: {
      getAnswer() {
        this.answer = 'Tauseed Zaman'
        // this.answer = 'Thinking...'
        // axios
        //   .get('https://yesno.wtf/api')
        //   .then(response => {
        //     this.answer = response.data.answer
        //   })
        //   .catch(error => {
        //     this.answer = 'Error! Could not reach the API. ' + error
        //   })
      }
    }
}
</script>

<style>

</style>