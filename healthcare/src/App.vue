<template>
  <v-app id="app">
    <div>
      <SideBar />
      <TopBar />
    </div>
    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script lang="ts">
import Vue from "vue";
import SideBar from "./components/Navigation/SideBar.vue";
import TopBar from "./components/Navigation/TopBar.vue";

export default Vue.extend({
  name: "App",

  components: {
    SideBar,
    TopBar,
  },
  data: () => ({}),
});
</script>

<style lang="scss">
@import "styles.scss";
</style>
