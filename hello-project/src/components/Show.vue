<template>
  <div class="show">
      <h4 v-for="(user,index) in users" :key=index> {{user.name}} == {{user.email}} </h4>
  </div>
</template>

<script>
export default {
    name : 'Show',
    props: ["users"],
};
</script>

<style>

</style>