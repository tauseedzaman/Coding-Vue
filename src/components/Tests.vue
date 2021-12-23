
<template>
  <h1>Just Tests</h1>

  <span v-once>This will never change: {{ msg }}</span>
  <br>
  <p>Using mustaches: <span v-html="rawHtml"></span></p>
</template>

<script>
export default {
    data(){
        return{
            msg:"hello world",
            rawHtml:"<p>tauseedzaman</p>"
        }
    }
}
app.component('save-button', {
  created() {
    // Debouncing with Lodash
    this.debouncedClick = _.debounce(this.click, 500)
  },
  unmounted() {
    // Cancel the timer when the component is removed
    this.debouncedClick.cancel()
  },
  methods: {
    click() {
      // ... respond to click ...
    }
  },
  template: `
    <button @click="debouncedClick">
      Save
    </button>
  `
});
</script>

<style>

</style>