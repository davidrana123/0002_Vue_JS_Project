<template>
 <h1>Hellow Vue Js</h1> 
 <Hello :homeTitle=" homeTitle" :allUsers="users"/>
</template>

<script>
import Hello from "./components/Hello"

export default {
  name: 'App',
  components: {
   Hello
  },
  data(){
    return{
       homeTitle: "Hello my first vue cli app",
      users: ["david rana" ,"shuhana devi","jeenu rana"],
      };
      },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
