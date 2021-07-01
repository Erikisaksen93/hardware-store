<template>
  <div class="navbar is-transparent">
    <div class="navbar-brand">
      <img :src="link" alt="loading" />
    </div>
  </div>
</template>

<script>
export default {
  name: "NavBar",
  data() {
    return {
      link: "https://i.ibb.co/RbgFzn6/logo.png",
    };
  },
  props: {
    msg: String,
  },
};
</script>


<style scoped>
</style>
