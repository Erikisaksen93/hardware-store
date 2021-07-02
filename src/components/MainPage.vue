<template>
  <div>
    <div class="section">
      <div class="columns">
        <div class="column is-one-fifth">
          <img :src="datakomponenter[0].prosessor.img" />
        </div>
        <div class="column is-three-fifth" style="margin-top: 2rem">
          <h1 class="title is-1" style="font-size: 1.5em">
            {{ datakomponenter[0].prosessor.navn }}
          </h1>
          <h3 class="subtitle is-3" style="font-size: 1em">
            {{ datakomponenter[0].prosessor.beskrivelse }}
          </h3>
        </div>
        <div
          class="column is-one-fifth"
          style="margin-top: 2rem; padding-left: 8rem"
        >
          <h1 class="title is-1" style="font-size: 1.5em">PRIS</h1>
          <h3 class="subtitle is-3" style="font-size: 1em">99 000,-</h3>
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
  border: none;
}
</style>