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
@import url('https://fonts.googleapis.com/css2?family=Pacifico&display=swap');
.name {
  background: -webkit-linear-gradient(19deg, #21d4fd 0%, #b721ff 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  font-family: 'Pacifico', cursive;
  font-size: 25px;
  letter-spacing: 0.2rem;
}
</style>