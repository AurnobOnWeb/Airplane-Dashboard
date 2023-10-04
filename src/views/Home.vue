<template>
  <v-app :style="{ background: $vuetify.theme.themes.light.colors.primary }">
    <SideBar />
    <v-main>
      <v-container class="px-6 mt-n2" fluid>
        <v-row>
          <v-col cols="12" sm="4">
            <v-card
              color="#B49239"
              theme="dark"
              class="rounded-xl"
              height="150"
            >
              <div class="d-flex flex-no-wrao justify-space-between">
                <div>
                  <v-card-title class="text-h5 mt-10">
                    Boleng 787
                  </v-card-title>
                  <v-card-subtitle>$589</v-card-subtitle>
                </div>
                <v-img
                  src="../assets/plane1.png"
                  class="mr-4 mt-5"
                  absolute
                  max-height="120"
                ></v-img>
              </div>
            </v-card>
          </v-col>
          <v-col cols="12" sm="4">
            <v-card
              color="#425C5A"
              theme="dark"
              class="rounded-xl"
              height="150"
            >
              <div class="d-flex flex-no-wrao justify-space-between">
                <div>
                  <v-card-title class="text-h5 mt-10">
                    Boleng 787
                  </v-card-title>
                  <v-card-subtitle>$589</v-card-subtitle>
                </div>
                <v-img
                  src="../assets/plane2.png"
                  class="mr-4 mt-5"
                  absolute
                  max-height="120"
                ></v-img>
              </div>
            </v-card>
          </v-col>
          <v-col cols="12" sm="4">
            <v-card
              color="#B49239"
              theme="dark"
              class="rounded-xl"
              height="150"
            >
              <div class="d-flex flex-no-wrao justify-space-between">
                <div>
                  <v-card-title class="text-h5 mt-10">
                    Boleng 787
                  </v-card-title>
                  <v-card-subtitle>$589</v-card-subtitle>
                </div>
                <v-img
                  src="../assets/plane3.png"
                  class="mr-4 mt-5"
                  absolute
                  max-height="120"
                ></v-img>
              </div>
            </v-card>
          </v-col>

          <v-col cols="12" sm="4" class="mt-n4">
            <v-card class="mx-auto" max-height="670px" min-height="380px">
              <v-card-item title="Doughnut">
                <Doughnuts />
              </v-card-item>
            </v-card>
          </v-col>
          <v-col cols="12" sm="8" class="mt-n4">
            <v-card class="mx-auto" max-height="620px" min-height="350px">
              <v-card-item title="Bubble">
                <Bubbles />
              </v-card-item>
            </v-card>
          </v-col>
          <v-col cols="12" sm="8" class="mt-n4">
            <v-card class="mx-auto" max-height="auto" min-height="200px">
              <v-card-item title="Last Trips">
                <template v-slot:subtitle>OverView Of last Month</template>
              </v-card-item>
              <v-card-text class="py-0 mt-n4">
                <v-row align="center" no-gutters>
                  <v-col cols="12">
                    <v-list lines="two">
                      <v-list-item
                        v-for="folder in folders"
                        :key="folder.title"
                        :title="folder.title"
                        :subtitle="folder.subtitle"
                      >
                        <template v-slot:prepend>
                          <v-avatar>
                            <v-img :src="folder.img"></v-img>
                          </v-avatar>
                        </template>
                        <template v-slot:append>
                          <v-btn
                            size="large"
                            color="#B49239"
                            icon="mdi mdi-airplane-off"
                          ></v-btn>
                        </template>
                      </v-list-item>
                    </v-list>
                  </v-col>
                </v-row>
              </v-card-text>
            </v-card>
          </v-col>
          <v-col cols="12" sm="4" class="mt-n4">
            <v-card max-height="355px" min-height="200px">
              <v-card-item title="Bar Chart">
                <BarCharts class="mt-n4" />
              </v-card-item>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import SideBar from "@/components/SideBar.vue";
import Doughnuts from "@/components/Doughnuts.vue";
import Bubbles from "@/components/Bubbles.vue";
import BarCharts from "@/components/BarCharts.vue";

export default {
  data: () => ({
    folders: [
      {
        subtitle: "john doe",
        title: "john@gmail.com",
        img: "../assets/1.jpg",
      },
      {
        subtitle: "john doe",
        title: "john@gmail.com",
        img: "../assets/1.jpg",
      },
    ],
  }),
  components: {
    SideBar,
    Doughnuts,
    Bubbles,
    BarCharts,
  },
};
</script>
