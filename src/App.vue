<template>
  <div id="app">
    <div class="navbar">
      <NavBar />
    </div>
    <div class="menu-section">
      <div class="section">
        <div class="container">
          <Menu />
        </div>
      </div>
    </div>
    <div class="view-section">
      <div class="hero">
        <div class="container">
          <MainPage />
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
      model: {
        datakomponenter: [
          {
            prosessor: [
              {
                navn: "Intel",
                modell: "i9-11900k",
              },
            ],
            skjermkort: [
              {
                navn: "Nvidia",
                modell: "ASUS Geforce 3080ti ROG STRIX OC",
              },
            ],
            minne: [
              {
                navn: "HyperX Fury RGB DDR4",
                modell: "3200MHZ 32GB",
              },
            ],
            lagring: [
              {
                navn: "WD BLACK",
                modell: "SN850 1TB M.2 SSD",
              },
            ],
            strøm: [
              {
                navn: "Corsair",
                modell: "RM850 - 850W PSU",
              },
            ],
          },
        ],
        TV: [
          {
            LG: [
              {
                navn: `LG 65" 4K NanoCell Smart TV`,
                modell: "65NANO81",
              },
            ],
            samsung: [
              {
                navn: `Samsung 85" QLED 4K Smart TV`,
                modell: "QE85Q60",
              },
            ],
          },
        ],
      },
    };
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins&display=swap");

#app {
  margin: 0;
  padding: 0;
}
.container {
}
</style>
