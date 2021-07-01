<template>
  <div id="app">
    <NavBar />
  </div>
</template>

<script>
import NavBar from "./components/NavBar";

export default {
  name: "App",
  components: {
    NavBar,
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
#app {
}
</style>
