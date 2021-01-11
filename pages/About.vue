<template>
  <v-container fluid class="About">
    <v-row class="justify-center" no-gutters>
      <transition appear>
        <v-col cols="12">
          <div
            class="text-center mt-4 text-subtitle-1 text-md-h6 text-lg-h6 text-xl-h5 font-weight-bold"
            style="color: rgb(116, 166, 76)"
          >
            About
          </div>
          <div
            class="text-center text-h5 text-sm-h4 text-md-h3 text-lg-h3 text-xl-h2 font-weight-bold"
          >
            自己紹介
          </div>
        </v-col>
      </transition>
    </v-row>
    <v-row
      align-content="center"
      justify="center"
      class="mt-3 mt-md-10 mt-lg-10 mt-xl-10"
    >
      <transition appear name="profile">
        <v-col
          :cols="avatar.xs"
          :sm="avatar.sm"
          :md="avatar.md"
          :lg="avatar.lg"
          :xl="avatar.xl"
          class="pl-md-10 pl-lg-14 pl-xl-15"
          style="max-width: 500px"
        >
          <v-avatar min-width="150" size="200">
            <img :src="avatar.src" alt="myAvatar" />
          </v-avatar>
        </v-col>
      </transition>
      <transition appear name="profile">
        <v-col
          :cols="texts.xs"
          :sm="texts.sm"
          :md="texts.md"
          :lg="texts.lg"
          :xl="texts.xl"
          class="pr-md-10 pr-lg-14 pr-xl-15"
          style="max-width: 500px"
        >
          <div
            v-for="(text, index) in texts.text.split('\n')"
            :key="index"
            class="text-center text-justify text-body-1 text-sm-body-1 text-md-h6 text-lg-h5 text-xl-h5 font-weight-bold"
          >
            {{ texts.text }}
          </div>
        </v-col>
      </transition>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    avatar: {
      src: require('../assets/profile.jpg'),
      xs: 12,
      sm: 12,
      md: 6,
      lg: 4,
      xl: 6,
    },
    texts: {
      text: 'FirstLine\nSecondLine\nThirdLine\nLastLine',
      xs: 12,
      sm: 12,
      md: 6,
      lg: 4,
      xl: 6,
    },
  }),
}
</script>

<style lang="scss" scoped>
.About {
  color: rgb(60, 60, 60);
  text-align: center;
  font-size: 32px;
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

.profile-enter-active {
  transition: opacity 5s;
}

.profile-enter {
  opacity: 0;
}

.profile-enter-to {
  opacity: 1;
}
</style>
