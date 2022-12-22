<template>
  <div class="top-bar">
    <v-text-field
      class="top-bar__search-input"
      rounded
      label="Search"
      prepend-inner-icon="mdi-magnify"
      filled
      background-color="#FFFFFF"
      height="40px"
      dense
      color="blue"
    ></v-text-field>
    <div class="top-bar__right-col">
      <div>
        <img
          class="top-bar__notification-icon"
          src="@/assets/bell.png"
          alt="Bell"
        />
        <span class="top-bar__notification">9</span>
      </div>
      <img src="@/assets/circle.png" alt="Circle" />
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class TopBar extends Vue {}
</script>

<style lang="scss">
.top-bar {
  height: 88px;
  margin-left: 256px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.top-bar__search-input {
  margin: 24px 0px 24px 36px !important;
  max-width: 350px !important;
  color: "blue";
}

.top-bar__right-col {
  margin: 24px 38px 24px 0px !important;
  display: flex;
  align-items: center;
}

.top-bar__notification {
  position: absolute;
  width: 15px;
  height: 15px;
  right: 90px;
  top: 24px;
  background-color: #ff6760;
  font-size: 9px;
  border: solid 1px #ff6760;
  border-radius: 25px;
  color: white;
  font-weight: 600;
}

.top-bar__notification-icon {
  margin-right: 23px;
}
</style>
