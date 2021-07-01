<template>
  <div class="columns">
    <div class="column">
      <div class="navbar is-transparent">
        <div class="navbar-brand">
          <img :src="logo" alt="loading" />
        </div>
        <div class="column">
          <div class="navbar-start">
            <div class="navbar-item">
              <span class="icon-text">
                <span class="icon">
                  <i class="fas fa-home"></i>
                </span>
                <span><a>Home</a></span>
              </span>
            </div>
            <div class="navbar-item">
              <span class="icon-text">
                <span class="icon">
                  <i class="fas fa-percent"></i>
                </span>
                <span><a>Ukens tilbud</a></span>
              </span>
            </div>
            <div class="navbar-item">
              <span class="icon-text">
                <span class="icon">
                  <i class="fas fa-gift-card"></i>
                </span>
                <span><a>Gavekort</a></span>
              </span>
            </div>
            <div class="navbar-item">
              <span class="icon-text">
                <span class="icon">
                  <i class="fas fa-user-headset"></i>
                </span>
                <span><a>Kundestøtte</a></span>
              </span>
            </div>
            <div class="navbar-end">
              <div class="navbar-item">
                <span class="icon-text">
                  <span class="icon">
                    <i class="fas fa-shopping-cart"></i>
                  </span>
                  <span><a>Handlekurv</a></span>
                </span>
              </div>
            </div>
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
      logo: "https://i.ibb.co/3WMLcjh/logo.png",
      links: {},
    };
  },
  props: {
    msg: String,
  },
};
</script>


<style scoped>
.navbar-brand {
  width: 400px;
  height: auto;
}
.navbar-start {
  margin-left: 15vw;
  font-size: 1.5em;
  margin-top: 4rem;
}
.navbar-item {
  margin-left: 3rem;
}
.icon {
  margin-top: -0.2rem;
}
.navbar a {
  color: black;
}
</style>
