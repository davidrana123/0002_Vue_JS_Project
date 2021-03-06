<template>
  <AddUser @add-user="storeUser"/>
  <Show  :users="users"/> 
</template>

<script>
import AddUser from "./components/AddUser";
import Show from "./components/Show";
import axios from "axios"
export default {
  name: "App",
  components: {
    AddUser,
    Show,
  },
  data(){
    return{
      homeTitle: "Hello my first vue app",
      users: [],
    };
  },
  methods: {
    storeUser: function(user){
       this.users = [user,...this.users];
    }, 
  },
  async created(){
    try{
        const response = await axios.get(
          "https://jsonplaceholder.typicode.com/users"
          );
          console.log(response.data);
    }catch(error){
      console.log(error);
    }
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
