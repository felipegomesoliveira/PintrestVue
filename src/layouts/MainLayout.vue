<template>
  <v-app>
    <v-app-bar height="100" app color="white" flat>
      <v-layout align-center>
        <v-flex>
          <v-text-field prepend-inner-icon="mdi-magnify" label="Search" flat solo class="mt-7" color="grey"></v-text-field>
        </v-flex>
        <v-flex style="position:relative; left:80%;">
            <v-btn height="48" class="mx-2 ml-4">
                <v-icon> mdi-compare-vertical </v-icon>
            </v-btn>

            <v-btn height="48" class="ml-2" dark>
                <v-icon> mdi-plus </v-icon>
            </v-btn>
        </v-flex>
      </v-layout>
      <v-spacer></v-spacer>
    </v-app-bar>

    <v-navigation-drawer app permanent>
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="text-h6">
            <v-list-item-avatar>
              <v-img
                width="10"
                lazy-src="https://logos-world.net/wp-content/uploads/2020/09/Pinterest-Logo-2011-present.png"
                src="https://logos-world.net/wp-content/uploads/2020/09/Pinterest-Logo-2011-present.png"
              />
            </v-list-item-avatar>
          </v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense nav>
        <v-list-item v-for="item in items" :key="item.title" link>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <div class="mx-4 subtitle-2 gray--text">Insghts</div>

      <v-list dense nav>
        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-mail</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>Messages</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-bell</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>Notifications</v-list-item-title>
          </v-list-item-content>
          <v-list-item-avatar
            size="25"
            color="orange"
            class="white--text subtitle-2"
          >
            2
          </v-list-item-avatar>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <home-page />
    </v-main>
  </v-app>
</template>

<script>
import HomePage from "@/pages/HomePage.vue";

export default {
  components: {
    HomePage,
  },

  data: () => ({
    items: [
      { title: "Home", icon: "mdi-view-dashboard" },
      { title: "Recent", icon: "mdi-clock-time-three" },
      { title: "Following", icon: "mdi-account-heart" },
    ],

    items2: [
      { title: "Messagens", icon: "mdi-view-dashboard" },
      { title: "Notifications", icon: "mdi-image" },
    ],
  }),
};
</script>

<style>
</style>