<template>
  <v-container fluid class="Works">
    <v-row class="justify-center" no-gutters>
      <transition appear>
        <v-col cols="12">
          <div
            class="text-center mt-4 text-subtitle-1 text-md-h6 text-lg-h6 text-xl-h5"
            style="color: rgb(116, 166, 76)"
          >
            Works
          </div>
          <div
            class="text-center mb-10 text-h5 text-sm-h4 text-md-h3 text-lg-h3 text-xl-h2"
          >
            製作したWebページ
          </div>
        </v-col>
      </transition>
    </v-row>
    <v-spacer></v-spacer>
    <v-row justify="space-around" align-content="start" style="height: 70vh">
      <v-col
        v-for="card in cards"
        :key="card.title"
        :cols="card.xs"
        :sm="card.sm"
        :md="card.md"
        :lg="card.lg"
        :xl="card.xl"
      >
        <v-card class="mx-auto" max-width="400">
          <v-img
            class="white--text align-end pt-n100"
            height="200px"
            :src="card.src"
          >
            <v-card-title v-text="card.title"></v-card-title>
          </v-img>

          <v-card-subtitle class="pb-0" v-text="card.subtitle">
          </v-card-subtitle>

          <v-card-text class="text--primary" v-text="card.text"> </v-card-text>

          <v-card-actions>
            <v-btn color="orange" text> Share </v-btn>

            <v-btn color="orange" text> Explore </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    cards: [
      {
        title: 'Pre-fab homes',
        subtitle: 'This is example',
        src: 'https://cdn.vuetifyjs.com/images/cards/house.jpg',
        text:
          'brbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrb',
        xs: 12,
        sm: 12,
        md: 6,
        lg: 6,
        xl: 6,
      },
      {
        title: 'Favorite road trips',
        subtitle: 'This is example',
        src: 'https://cdn.vuetifyjs.com/images/cards/road.jpg',
        text:
          'brbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrbrb',
        xs: 12,
        sm: 12,
        md: 6,
        lg: 6,
        xl: 6,
      },
    ],
  }),
}
</script>

<style lang="scss" scoped>
.Works {
  color: rgb(60, 60, 60);
  font-size: 24px;
  font-weight: bold;
}

.v-enter-active {
  transition: opacity 2s;
}

.v-enter {
  opacity: 0;
}
.v-enter-to {
  opacity: 1;
}
</style>
