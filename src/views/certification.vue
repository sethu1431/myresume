<template>
  <div>
    <v-layout align-center justify-center wrap mt-3 pt-3 style="background:white">
      <v-flex xs12 md12 class="justify-center layout">
        <p class="heading">certifications</p>
      </v-flex>
      <v-flex xs12 md4 px-3>
        <v-virtual-scroll :items="certification" :item-height="300" height="250">
          <template v-slot="{ item }">
            <v-list-item class="pa-5">
              <v-img :src="item.image" aspect-ratio="1.5" :lazy-src="lazy" class="ma-5" contain>
                <template v-slot:placeholder>
                  <v-row class="fill-height ma-0" align="center" justify="center">
                    <v-progress-circular indeterminate color="indigo accent-3"></v-progress-circular>
                  </v-row>
                </template>
              </v-img>
            </v-list-item>
          </template>
        </v-virtual-scroll>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
import axios from "axios";
import lazy from '../assets/blurd.jpg'
export default {
  data() {
    return {
      certification: [],
      lazy: lazy
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
          e.data.certification.forEach(e => {
            this.certification.push(e);
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