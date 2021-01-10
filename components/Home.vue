<template>
  <section class="home">
    <v-container fluid fill-height class="home__content">
      <v-row>
        <transition appear>
          <v-col class="home__content-text">
            <h1>Ryo Takayama's</h1>
            <h1>PortFolio</h1>
          </v-col>
        </transition>
      </v-row>
    </v-container>
  </section>
</template>

<style lang="scss" scoped>
.home {
  width: 100%;
  height: 100%;
}

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
    font-weight: bold;
  }

  .v-enter-active {
    transition: opacity 3s;
  }

  .v-enter {
    opacity: 0;
  }
  .v-enter-to {
    opacity: 1;
  }
}
</style>
