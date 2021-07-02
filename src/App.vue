<template>
  <div id="app">
    <div class="navbar">
      <NavBar :itemsInCart="cartLength" />
    </div>
    <div class="columns">
      <div class="column is-two-fifths">
        <div class="menu-section">
          <div class="section">
            <div class="container">
              <Menu />
            </div>
          </div>
        </div>
      </div>
      <div class="column is-three-fifths">
        <div class="view-section">
          <div class="hero">
            <div class="container">
              <MainPage />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import NavBar from "./components/NavBar";
import MainPage from "./components/MainPage";
import Menu from "./components/Menu";

export default {
  name: "App",
  components: {
    NavBar,
    MainPage,
    Menu,
  },

  data() {
    return {
      datakomponenter: [],
      cart: [
        {
          type: "prosessor",
          navn: "Intel Core i17-19900KXX Prosessor",
          beskrivelse:
            "Socket-LGA9000x, 69-Core, 420-Thread, 9.5/16.2GHz, Rocket Lake, uten kjøler",
          pris: 99000,
          img: "https://www.komplett.no/img/p/200/1180155.jpg",
        },

        {
          type: "skjermkort",
          navn: "MSI GeForce RTX3080Ti SUPRIM X",
          beskrivelse: "Skjermkort, PCI-Express 4.0, 12GB GDDR6X, Ampere",
          pris: 125500,
          img: "https://www.komplett.no/img/p/200/1187638.jpg",
        },
      ],
    };
  },
  computed: {
    cartLength() {
      return this.cart.length;
    },
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins&display=swap");

#app {
  margin: 0;
  padding: 0;
  font-family: "Poppins", sans-serif;
}

.navbar-section {
  background-color: coral;
}

.menu-section {
  background-color: cornflowerblue;
}

.view-section {
}
</style>
