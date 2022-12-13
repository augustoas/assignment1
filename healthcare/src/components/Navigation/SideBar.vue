<template>
  <v-navigation-drawer app permanent class="side-nav" width="256">
    <div class="logo-nav">
      <img src="@/assets/logo-image.png" alt="Healthcare" />
    </div>
    <v-list flat>
      <v-subheader class="subtitle1">MEDICINE</v-subheader>
      <v-list-item-group v-model="selectedItem" color="primary">
        <v-list-item v-for="(item, i) in items" :key="i">
          <v-list-item-icon>
            <v-icon
              :color="getIconColor(i)"
              class="icon-nav"
              v-text="item.icon"
            ></v-icon>
          </v-list-item-icon>
          <v-list-item-content class="subtitle2">
            <span v-text="item.name"></span>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </v-navigation-drawer>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class SideBar extends Vue {
  public name = "SideBar";
  public selectedItem = 0;

  public items = [
    {
      name: "Dashboard",
      icon: "mdi-view-dashboard-outline",
      route: {
        name: "daily-opt",
      },
    },
    {
      name: "Appointments",
      icon: "mdi-view-dashboard",
      route: {
        name: "weekly-opt",
      },
    },
    {
      name: "Doctors",
      icon: "mdi-view-dashboard-outline",
      route: {
        name: "monthly-opt",
      },
    },
    {
      name: "Departments",
      icon: "mdi-view-dashboard-outline",
      route: {
        name: "monthly-opt",
      },
    },
    {
      name: "Patients",
      icon: "mdi-view-dashboard-outline",
      route: {
        name: "monthly-opt",
      },
    },
    {
      name: "Payments",
      icon: "mdi-view-dashboard-outline",
      route: {
        name: "monthly-opt",
      },
    },
    {
      name: "Help",
      icon: "mdi-view-dashboard-outline",
      route: {
        name: "monthly-opt",
      },
    },
  ];

  getIconColor(index) {
    return index === this.selectedItem ? "primary" : "var(--navbar-icon-color)";
  }
}
</script>

<style lang="scss" scoped>
.side-nav {
  box-shadow: 4px 0px 16px 0px #101e7314;
}

.logo-nav {
  margin: 24px 90px 30px 24px;
}

.subtitle1 {
  margin: 0px 90px 0px 24px;
  padding: 0px;
}

::v-deep .v-list-item {
  padding: 0px;
  align-self: center;
  margin: 10px 0px 0px 0px;

  .v-list-item__icon:first-child {
    margin-right: 10px;
  }

  .v-list-item__icon {
    margin: 0px 0px 0px 24px;
    align-self: center;
  }

  .v-list-item__content {
    flex: none;
  }
}

::v-deep .v-list-item:last-child {
  border-top: 1px solid #e8e8e8;
  margin-top: 10px;
  padding-top: 10px;
}
</style>
