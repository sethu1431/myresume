<template>
  <div>
    <v-app v-if="state">loading</v-app>
    <v-app else>
      <v-app-bar app color="white" dark>
        <div class="d-flex">
          <div class="name">Sethupathi Palanisamy</div>
        </div>
        <v-spacer></v-spacer>
        <a
          href="https://sethu1431.github.io/myresume-api/sethuresume.pdf"
          target="_blank"
          style="text-decoration:none"
          download
        >
          <v-btn class="mt-2 hidden-sm-and-down" color="indigo accent-4">
            <v-icon small class="pr-2" color="white">mdi-download</v-icon>Download Resume
          </v-btn>
        </a>
        <a
          href="https://sethu1431.github.io/myresume-api/sethuresume.pdf"
          target="_blank"
          style="text-decoration:none"
          download
        >
          <v-btn class="mt-2 hidden-md-and-up" fab small color="indigo accent-4">
            <v-icon small color="white">mdi-download</v-icon>
          </v-btn>
        </a>
      </v-app-bar>
      <v-main>
        <router-view />
      </v-main>
      <v-snackbar v-model="snackbar" :timeout="timeout" right shaped top>
        Connect with me on LinkedIn
        <template v-slot:action="{ attrs }">
          <v-btn color="blue" text v-bind="attrs" @click="snackbar = false">close</v-btn>
        </template>
      </v-snackbar>
    </v-app>
  </div>
</template>

<script>
export default {
  name: "App",
  data: () => ({
    snackbar: true,
    timeout: 6000,
    state: true
  }),
  mounted() {
    document.onreadystatechange = () => {
      if (document.readyState == "complete") {
        this.state = false;
      }
    };
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@500&display=swap");
.name {
  background: -webkit-linear-gradient(19deg, #21d4fd 0%, #b721ff 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  font-family: "Poppins", sans-serif;
  font-size: 20px;

  font-weight: 600;
  letter-spacing: 1.5px;
}
</style>