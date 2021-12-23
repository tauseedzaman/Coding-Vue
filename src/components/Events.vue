<template>
  <h1 class="text-center">Vue Events</h1>
  <a class="btn btn-info btn-lg" @click.once="doThis">Once</a>
  <hr />
  <input @keyup.enter="submit" class="form-control" />
  <br />
  <hr />
  <input @keyup.alt.enter="clear" class="form-control" />
<br />
  <hr />
  <!-- Ctrl + Click -->
<div @click.ctrl="doSomething">Do something</div>

<br />
  <hr />
  <button @click.right="rightMouseClick" class="btn btn-info btn-lg">Right Mouse Click Only</button>

  <br />
  <hr />
  <button @click.left="leftMouseClick" class="btn btn-danger btn-lg">Left Mouse Click Only</button>

  <br />
  <hr />
  <button @click.middle="middleMouseClick" class="btn btn-warning btn-lg">Middle Mouse Click Only</button>
</template>

<script>
export default {
    methods:{
        doThis(){
            alert("only once");
        },
    submit(){
        alert("yeah. submitted");
    },
    clear(){
        alert("clear at now....");
    },
    doSomething(){
        alert("doing something");
    },
    rightMouseClick(){
        alert("yeah. thanks for your suppert.");
    },
    leftMouseClick(){
        alert("yeah. thanks for left mouse clicking.");
    },
    middleMouseClick(){
        alert("yeah. thanks for middle mouse clicking.");
    }
    },
}
</script>

<style>
</style>