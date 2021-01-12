<template>
  <v-container
    fluid
    style="background-color: rgb(217, 234, 236)"
    class="py-12 my-12"
  >
    <v-row class="justify-center" no-gutters>
      <transition appear>
        <v-col cols="12">
          <div
            class="text-center mt-4 text-subtitle-1 text-md-h6 text-lg-h6 text-xl-h5 font-weight-bold"
            style="color: rgb(116, 166, 76)"
          >
            Works
          </div>
          <div
            class="text-center mb-10 text-h5 text-sm-h4 text-md-h3 text-lg-h3 text-xl-h2 font-weight-bold"
          >
            製作したWebページ
          </div>
        </v-col>
      </transition>
    </v-row>
    <v-row justify="space-around" align-content="start">
      <v-col
        v-for="card in cards"
        :key="card.title"
        :cols="card.xs"
        :sm="card.sm"
        :md="card.md"
        :lg="card.lg"
        :xl="card.xl"
      >
        <v-card class="mx-auto mb-8" max-width="400">
          <v-img height="200px" :src="card.src"> </v-img>
          <v-card-title v-text="card.title"></v-card-title>
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
