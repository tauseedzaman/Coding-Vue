<template >
<h4 class="text-success">Posts</h4>
  <ul >
      <li class="post" v-for="(item,i) in items" :key="i">
          <p>
              <b class="text-info">{{ item.auther }}</b>
              <br>
              <span>{{ item.message }}</span>
              <br>
              <small><i class="text-warning">{{ item.created_at }}</i></small>
          </p>
      </li>
  </ul>
</template>

<script>
export default {
    data(){
        return {
            items:[
                {
                    auther:"tauseed",
                    message:"hello how are you..",
                    created_at:"4 months ago"
                },
                 {
                    auther:"zaman",
                    message:"Nice meeting you..",
                    created_at:"6 months ago"
                },
                 {
                    auther:"jabran",
                    message:"Mee tooooo..",
                    created_at:"1 months ago"
                },
            ]
        }
    }
}
</script>

<style>
*{
    padding:0px;
    color:"white";
}
    .post{
        color:white;
        list-style:none;
        /* background-color:cyan; */
        padding:1px;
        border:1px solid red;

    }
    .post > p > b{
        color:"red";
    } 
</style>