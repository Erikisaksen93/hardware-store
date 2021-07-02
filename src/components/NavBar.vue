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
                <span><a :href="links.home">Home</a></span>
              </span>
            </div>
            <div class="navbar-item">
              <span class="icon-text">
                <span class="icon">
                  <i class="fas fa-percent"></i>
                </span>
                <span><a :href="links.home">Ukens tilbud</a></span>
              </span>
            </div>
            <div class="navbar-item">
              <span class="icon-text">
                <span class="icon">
                  <i class="fas fa-gift-card"></i>
                </span>
                <span><a :href="links.home">Gavekort</a></span>
              </span>
            </div>
            <div class="navbar-item">
              <span class="icon-text">
                <span class="icon">
                  <i class="fas fa-user-headset"></i>
                </span>
                <span><a :href="links.home">Kundestøtte</a></span>
              </span>
            </div>
            <div class="navbar-end">
              <div class="navbar-item">
                <span class="icon-text">
                  <span class="icon">
                    <i class="fas fa-shopping-cart"></i>
                  </span>
                  <span
                    ><a :href="links.home"
                      >Handlekurv ({{ itemsInCart }})
                    </a></span
                  >
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
import { model } from "../shared/data";
export default {
  name: "NavBar",
  data() {
    return {
      logo: "https://i.ibb.co/3WMLcjh/logo.png",
      links: {
        home: "../components/MainPage",
      },
    };
  },
  props: {
    msg: String,
    itemsInCart: Number,
  },
  created() {
    this.datakomponenter = { ...model.datakomponenter };
    this.tv = { ...model.TV };
  },
};
</script>


<style scoped>
.navbar-brand img {
  width: 250px;
  height: auto;
}
.navbar-start {
  margin-left: 15vw;
  font-size: 1.5em;
  margin-top: 4rem;
}
.navbar-item {
  margin-left: 3rem;
  color: black;
}
.navbar-item:hover {
  color: #5999be;
  opacity: 1;
  -webkit-transform: scale(1.2);
  transform: scale(1.2);
}
.icon {
  margin-top: -0.2rem;
}
.navbar a {
  color: black;
}
.navbar a:hover {
  color: #5999be;
  opacity: 1;
  -webkit-transform: scale(1.2);
  transform: scale(1.2);
}
</style>
