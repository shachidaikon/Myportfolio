<template>
  <v-app>
    <!-- <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
      color="rgb(249,249,249)"
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer> -->
    <v-app-bar :clipped-left="clipped" fixed app color="rgb(249,249,249)">
      <!-- <v-app-bar-nav-icon @click.stop="drawer = !drawer" /> -->
      <v-toolbar-title class="colorrize" v-text="title" />
      <v-spacer />
    </v-app-bar>
    <v-main class="whitenize">
      <nuxt />
    </v-main>
  </v-app>
</template>

<script>
import { mdiAccount } from '@mdi/js'
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/',
        },
        {
          icon: mdiAccount,
          title: 'About',
          to: '/About',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Works',
          to: '/Works',
        },
      ],
      miniVariant: false,
      title: "Shachi Daikon's Portfolio",
    }
  },
}
</script>

<style lang="scss" scoped>
.colorrize {
  color: rgb(116, 166, 76);
  font-weight: bold;
}
.whitenize {
  background-color: rgb(249, 249, 249);
}
</style>
