<template>
  <div>
    <div class="section">
      <div
        class="columns"
        v-for="(items, index) in datakomponenter"
        :key="index"
      >
        <div class="column is-one-fifth">
          <img :src="items.img" />
        </div>
        <div class="column is-three-fifth" style="margin-top: 2rem">
          <h1 class="title is-1" style="font-size: 1.5em">
            {{ items.navn }}
          </h1>
          <h3 class="subtitle is-3" style="font-size: 1em">
            {{ items.beskrivelse }}
          </h3>
        </div>
        <div
          class="column is-one-fifth"
          style="margin-top: 2rem; padding-left: 8rem"
        >
          <h1 class="title is-1" style="font-size: 1.5em">PRIS</h1>
          <h3 class="subtitle is-3" style="font-size: 1em">
            {{ items.pris }},-
          </h3>
        </div>
        <div class="column is-one-fifth" style="margin-top: 2rem">
          <input type="number" class="selectAmount" />
          <div class="buttons">
            <button class="button is-info">Kjøp</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { model } from "../shared/data";
import deepClone from "deep-clone";

export default {
  name: "MainPage",
  props: {
    msg: String,
  },
  created() {
    this.datakomponenter = deepClone(model.datakomponenter);
    this.tv = deepClone(model.TV);
  },

  data() {
    return {
      datakomponenter: null,
      tv: null,
    };
  },
};
</script>

<style scoped>
img {
  width: 1200px;
  height: auto;
}

.selectAmount {
  width: 3.5vw;
  height: 4vh;
  font-weight: bolder;
  text-align: center;
  border: solid 2px black;
  border-radius: 5%;
}
</style>