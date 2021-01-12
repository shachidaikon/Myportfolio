<template>
  <section class="home">
    <Home />
    <About />
    <Works />
    <Skill />
    <Footers />
  </section>
</template>

<script>
import Home from '~/components/Home.vue'
import About from '~/components/About.vue'
import Works from '~/components/Works.vue'
import Skill from '~/components/Skill.vue'
import Footers from '~/components/Footers.vue'

export default {
  components: {
    Home,
    About,
    Works,
    Skill,
    Footers,
  },
}
</script>

<style lang="scss" scoped>
// .home {
//   padding-bottom: 50px;
// }
</style>
