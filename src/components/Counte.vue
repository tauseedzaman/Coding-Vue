<template>
    <div class="counter bg-info">
        <h1 v-bind="counter"></h1>
        <button @click="add_counter()">Counter</button>
    </div>
</template>

<style >

</style>

<script>
export default {
    counter:0,
    add_counter:()=>{
        this.counter = this.counter+1
    }
}
</script>