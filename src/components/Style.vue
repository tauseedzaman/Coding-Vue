<template>
  <h1 class="" :class="{isvalid,info} " >Hello World</h1>
  <button @click="toggleborder">Toggle Border</button>
</template>

<script>
export default {
    data(){
        return {
            isvalid:false,
            info:true
        }
    },
    methods:{
        toggleborder(){
            this.info = !this.info
        }
    }
}
</script>

<style>
.isvalid{
    color:"green";
    color:"green";
    background:"cyan";
}
.info{
    border: 2px solid red;
}
</style>