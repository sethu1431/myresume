<template>
  <v-app>
    <v-app-bar app color="white" dark>
      <div class="d-flex">
        <div class="name">Sethupathi palanisamy</div>
      </div>
      <v-spacer></v-spacer>
    </v-app-bar>
    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",
  data: () => ({
    //
  })
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Lobster&display=swap");
.name {
  color: black;
  font-family: "Lobster", cursive;
  font-size: 25px;
  letter-spacing: 0.2rem;
}
</style>