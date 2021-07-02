<template>
  <div id="app">
    <div class="navbar">
      <NavBar />
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
    };
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
  background-color: darkcyan;
}
</style>
