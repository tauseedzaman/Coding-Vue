<template>
  Hello world
</template>

<script>
export default {
    props: {
    user: {
      type: String,
      required: true
    }
  },
    setup(props){
        console.log(props.user);
    },
    data(){
        console.log("inside data")
        return{
            x:"Hello"
        }
    },
    watch(){
        console.log("inside watch")
    },
    computed: {
        // x:"World"
    },
    mount() {
        console.log('inside onmount')
    },
    methods:{
        Test(){
            console.log('inside methods')
        }
    }
}
</script>

<style>

</style>