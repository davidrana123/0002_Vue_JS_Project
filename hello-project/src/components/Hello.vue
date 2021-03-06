<template>
    <div class="hello">
        <h1>{{homeTitle}}</h1>
        <p>Hello vue js student</p>
        <h4 v-for="(user,index) in allUsers" :key="index"> {{index}} = {{user}} </h4>
        <button @click="callFunction">Click me</button>
    </div>
</template>

<script>
export default {
  name: 'Hello',
  props: ["homeTitle","allUsers"],
  data(){
      return{
          title: "My first vue cli application",
          };
    },
     methods:{
        callFunction: function(){
          console.log("hello click enent");
        },
      },
};
</script>


<style>
h1{
    color: green;
}
</style>