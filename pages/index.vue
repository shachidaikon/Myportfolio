<template>
  <section class="home">
    <Home />
    <About />
    <Works />
  </section>
</template>

<script>
import Home from '~/components/Home.vue'
import About from '~/components/About.vue'
import Works from '~/components/Works.vue'

export default {
  components: {
    Home,
    About,
    Works,
  },
}
</script>

<style lang="scss" scoped>
// .home {
//   padding-bottom: 50px;
// }
</style>
