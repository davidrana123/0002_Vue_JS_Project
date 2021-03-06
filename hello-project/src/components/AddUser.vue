<template>
  <form @submit="storeUser">
      <input type="text" placeholder="Enter the name..." v-model="name">
      <br><br>
      <input type="email" placeholder="Enter Email.." v-model="email">
      <br><br>
      <input type="submit" value="Add User">
</form>
</template>

<script>
export default {
    name: 'AddUser',
    data(){
        return{
            name : '',
            email: ''
        };
    },
    methods: {
        storeUser: function(e){
            e.preventDefault();
            this.$emit('add-user', {name: this.name,email: this.email});
            this.name = "";
            this.email = "";
        },
    },
};
</script>

<style>

</style>