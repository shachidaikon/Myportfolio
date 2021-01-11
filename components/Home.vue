<template>
  <section>
    <v-container fluid fill-height class="home__content">
      <v-row>
        <transition appear>
          <v-col class="home__content-text">
            <div
              class="text-center text-h3 text-sm-h2 text-md-h1 text-lg-h1 text-xl-h1 font-weight-bold"
              style="
                color: rgb(249, 249, 249);
                text-shadow: 1px 2px 3px #808080;
              "
            >
              Shachi Daikon's
            </div>
            <div
              class="text-center text-h3 text-sm-h2 text-md-h1 text-lg-h1 text-xl-h1 font-weight-bold"
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

<style lang="scss" scoped>
.home__content {
  background: url('../assets/senro.png');
  background-size: cover;
  background-position: center center;
  width: 100%;
  height: 92vh;

  &-text {
    color: rgb(249, 249, 249);
    text-align: center;
    font-size: 48px;
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
}
</style>
