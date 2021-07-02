<template>
  <div>
    <div class="section">
      <div class="columns">
        <div class="column is-one-fifth">
          <img :src="datakomponenter[0].prosessor[0].img" />
        </div>
        <div class="column is-three-fifth">
          <p>Info</p>
        </div>
        <div class="column is-one-fifth">
          <p>Pris:</p>
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
</style>