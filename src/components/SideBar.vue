<template>
  <v-navigation-drawer v-model="drawer" color="#425C5A" class="rounded-e-xl">
    <v-sheet color="#3D5654" class="pa-4 rounded-te-xl text-center">
      <v-progress-circular
        model-value="80"
        color="#B49239"
        :size="100"
        :width="2"
      >
        <v-avatar size="85">
          <v-img src="../assets/4.png"></v-img>
        </v-avatar>
      </v-progress-circular>
      <div class="mt-4">Dahboard</div>
      <span class="mb-6 text-caption">Dashboard@gmail.com</span>
    </v-sheet>
    <v-list>
      <v-list-item
        m
        v-for="(item, i) in link"
        :key="i"
        :value="item"
        active-class="border"
        :ripple="false"
      >
        <template v-slot:prepend>
          <v-icon :icon="item.icon" color="#b49239"></v-icon>
        </template>
        <v-list-item-title v-text="item.text"></v-list-item-title>
      </v-list-item>
    </v-list>
    <h5 class="ml-5 text-yellow-darken-2">Active Users</h5>
    <v-row align="center" class="spacer ml-16 mt-4" no-gutters>
      <v-col cols="4" sm="2" md="1">
        <v-avatar size="36px">
          <v-img alt="" src="../assets/1.jpg"></v-img>
        </v-avatar>
      </v-col>
      <v-col cols="4" sm="2" md="1">
        <v-avatar size="36px">
          <v-img alt="" src="../assets/2.jpg"></v-img>
        </v-avatar>
      </v-col>
      <v-col cols="4" sm="2" md="1">
        <v-avatar size="36px">
          <v-img alt="" src="../assets/3.png"></v-img>
        </v-avatar>
      </v-col>
      <v-col cols="4" sm="2" md="1">
        <v-avatar size="36px">
          <v-img alt="" src="../assets/4.png"></v-img>
        </v-avatar>
      </v-col>
      <v-col cols="4" sm="2" md="1">
        <v-avatar size="36px" color="#B49239"> +70 </v-avatar>
      </v-col>
    </v-row>
    <div style="position: relative; z-index: 9999" class="mt-2">
      <v-img src="../assets/map.png" contain max-height="200"></v-img>
    </div>
  </v-navigation-drawer>
</template>

<script setup>
import { ref } from "vue";
const link = [
  { text: "DASHBOARD", icon: "mdi mdi-home-outline" },
  { text: "FLIGHT", icon: "mdi mdi-airplane-off" },
  { text: "WALLET", icon: "mdi mdi-wallet-outline" },
  { text: "REPORT", icon: "mdi mdi-file-chart-outline" },
  { text: "STATSTICS", icon: "mdi mdi-chart-pie" },
  { text: "SETTING", icon: "mdi mdi-cog-outline" },
];
const drawer = ref(null);
</script>
<script>
export default {
  data: () => ({
    cards: ["Today", "Yesterday"],
    drawer: null,
  }),
};
</script>
