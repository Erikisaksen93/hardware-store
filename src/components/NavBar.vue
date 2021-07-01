<template>
  <div class="columns">
    <div class="column">
      <div class="navbar is-transparent">
        <div class="navbar-brand">
          <img :src="link" alt="loading" />
        </div>
        <div class="column"></div>
        <div class="navbar-start">
          <div class="navbar-item">Hjem</div>
          <div class="navbar-item">Ukens tilbud</div>
          <div class="navbar-item">Gavekort</div>
          <div class="navbar-item">Kundestøtte</div>
          <div class="navbar-end">
            <div class="navbar-item">Handlekurv</div>
          </div>
        </div>
      </div>
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
.navbar-start {
  margin-left: 25vw;
  font-size: 1.5em;
  margin-top: 2.1rem;
}
</style>
