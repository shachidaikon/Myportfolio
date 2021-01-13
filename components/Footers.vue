<template>
  <v-footer padless class="mt-12 pt-12">
    <v-card
      flat
      tile
      width="100%"
      class="text-center"
      style="background-color: rgb(188, 213, 55)"
    >
      <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon.src"
          class="mx-4"
          icon
          :href="icon.link"
        >
          <v-icon size="40px">
            {{ icon.src }}
          </v-icon>
        </v-btn>
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text font-weight-bold">
        {{ new Date().getFullYear() }} — <strong>Contact</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
import { mdiGithub } from '@mdi/js'
export default {
  data: () => ({
    icons: [
      {
        src: mdiGithub,
        link: 'https://github.com/shachidaikon',
      },
    ],
  }),
}
</script>
