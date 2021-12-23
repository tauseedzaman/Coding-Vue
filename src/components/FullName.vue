<template>
  <h1>Name Test</h1>
  <div id="demo">{{ fullName }}</div>
</template>

<script>
export default {
    data() {
    return {
      firstName: 'Tauseed',
      lastName: 'Zaman'
    }
  },
  computed: {
    fullName() {
      return this.firstName + ' ' + this.lastName
    }
  }
}
</script>

<style>

</style>