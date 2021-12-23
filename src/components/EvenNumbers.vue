<template>
  <h1>Just Even Numbers 😈</h1>
  <ul>
      <li v-for="n in 10" :key="n">{{ n }}</li>
  </ul>
</template>

<script>
export default {
    data(){
        return{
            numbers:[1,2,3,4,5,6,7,8]
        }
    },
    computed:{
        evenNumbers(){
            return this.numbers.filter(number => number % 2 === 0)
        }
    }


}
</script>

<style>

</style>