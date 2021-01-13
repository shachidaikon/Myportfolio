<template>
  <v-container fluid class="About py-12 my-12">
    <v-row class="justify-center" no-gutters>
      <transition appear>
        <v-col cols="12">
          <div
            class="text-center text-subtitle-1 text-md-h6 text-lg-h6 text-xl-h5 font-weight-bold pt-n4"
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
    <v-row class="mt-10 mt-md-10 mt-lg-10 mt-xl-10 justify-center align-center">
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
          <div class="text-justify text-h6 font-weight-bold mb-4">
            高山 伶(タカヤマ リョウ)
          </div>
          <div
            class="text-justify text-body-2 text-sm-body-1 text-md-body-1 text-lg-body-1 text-xl-body-1 font-weight-bold"
          >
            <p style="white-space: pre-wrap">{{ texts.text }}</p>
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
      lg: 6,
      xl: 6,
    },
    texts: {
      text:
        '仙台市出身、平成11年生まれの大学３年生。\n\n明治大学総合数理学部に在学中。ゼミの活動を通して、世の中にある課題を発見し、情報技術を使って解決へアプローチする手法を学ぶ。\n\nコロナ禍でのオンラインオープンキャンパスで、所属する研究室の特設Webページ制作に携わり、Webの世界に足を踏み入れる。\n\n現在は祖父母宅に居候し、祖父母の介助をしながらWebアプリケーション制作に勤しむ。',
      xs: 12,
      sm: 12,
      md: 6,
      lg: 6,
      xl: 6,
    },
  }),
}
</script>

<style lang="scss" scoped>
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
</style>
