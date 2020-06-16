<template>
  <div>
    <v-layout align-center justify-center wrap mt-3 pt-3 style="background:white">
      <v-flex xs12 md12 class="justify-center layout">
        <p class="heading">my album</p>
      </v-flex>
      <v-flex xs12 md8 px-3>
        <v-layout align-center justify-center row wrap>
          <v-flex v-for="(i,j) in album" :key="j" xs6 md4 pa-3>
            <v-hover v-slot:default="{ hover }">
              <v-img :src="i.image" contain aspect-ratio="2">
                <template v-slot:placeholder>
                  <v-row class="fill-height ma-0" align="center" justify="center">
                    <v-progress-circular indeterminate color="indigo accent-3"></v-progress-circular>
                  </v-row>
                </template>
                <v-expand-transition>
                  <div
                    v-if="hover"
                    class="d-flex transition-fast-in-fast-out v-card--reveal indigo accent-4 white--text"
                    style="height: 100%;"
                  >{{ i.theme }}</div>
                </v-expand-transition>
              </v-img>
            </v-hover>
          </v-flex>
        </v-layout>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      album: []
    };
  },
  mounted() {
    this.update();
  },
  methods: {
    update() {
      let url = "https://sethu1431.github.io/myresume-api/myresume.json";
      try {
        axios.get(url).then(e => {
          console.table(e.data.album);
          e.data.album.forEach(e => {
            this.album.push(e);
          });
        });
      } catch (err) {
        console.log(err);
      }
    }
  }
};
</script>

<style scoped>
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: 0.8;
  position: absolute;
  width: 100%;
  padding: 0 10px;
}
</style>