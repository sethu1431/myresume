<template>
  <div>
    <v-layout align-center justify-center wrap mt-3 pt-3 style="background:white">
      <v-flex xs12 md12 class="justify-center layout">
        <p class="heading">certifications</p>
      </v-flex>
      <v-flex xs12 md8 px-3 >
        <center>  Will be Upload Soon </center>
        <v-layout align-center justify-center row wrap>
          <v-flex v-for="(i,j) in images" :key="j" xs6 md4 pa-3>
            <v-hover v-slot:default="{ hover }">
              <v-img :src="i.pathLong" contain class="img" aspect-ratio="3">
                <template v-slot:placeholder>
                  <v-row class="fill-height ma-0" align="center" justify="center">
                    <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                  </v-row>
                </template>
                <v-expand-transition>
                  <div
                    v-if="hover"
                    class="d-flex transition-fast-in-fast-out v-card--reveal indigo accent-4 white--text"
                    style="height: 100%;"
                  >{{ content[j] }}</div>
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
export default {
  data() {
    return {
      images: [],
      content: [
        
      ]
    };
  },
  mounted() {
    this.importAll(require.context("../assets/certifications/", true, /\.png$/));
  },
  methods: {
    importAll(r) {
      r.keys().forEach(key =>
        this.images.push({ pathLong: r(key), pathShort: key })
      );
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