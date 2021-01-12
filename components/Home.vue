<template>
  <section>
    <v-container fluid fill-height class="home__content mb-12">
      <v-row>
        <transition appear>
          <v-col class="home__content-text">
            <div
              class="text-center text-h4 text-sm-h2 text-md-h1 text-lg-h1 text-xl-h1 font-weight-bold"
              style="
                color: rgb(249, 249, 249);
                text-shadow: 1px 2px 3px #808080;
              "
            >
              Shachi Daikon's
            </div>
            <div
              class="text-center text-h4 text-sm-h2 text-md-h1 text-lg-h1 text-xl-h1 font-weight-bold"
              style="
                color: rgb(249, 249, 249);
                text-shadow: 1px 2px 3px #808080;
              "
            >
              Portfolio
            </div>
          </v-col>
        </transition>
      </v-row>
    </v-container>
  </section>
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
.home__content {
  background: url('../assets/senro.png');
  background-size: cover;
  background-position: center center;
  width: 100%;
  height: 92vh;

  .About {
    text-align: center;
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
}
</style>
