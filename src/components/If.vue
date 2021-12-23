<template>
 
<center>
    <select name="" id="" v-model="me">
        <option selected value="😎">😎</option>
        <option value="🎃">🎃</option>
        <option value="😳">😳</option>
        <option value="☹️">☹️</option>
    </select>
</center>
 <h1> i am 
      <span v-if="me === '😎'">😎</span>
      <span v-else-if="me === '😳'">😳</span>
      <span v-else-if="me === '☹️'">☹️</span>
      <span v-else>🎃</span>
</h1>
</template>

<script>
export default {
    data(){
        return{
            me:""
        }
    },
    methods:{
    }

}
</script>

<style>

</style>