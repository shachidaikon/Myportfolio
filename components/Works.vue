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
    <v-row justify="center" align-content="center">
      <v-col
        v-for="card in cards"
        :key="card.title"
        cols="12"
        sm="12"
        md="12"
        lg="6"
        xl="6"
      >
        <v-card class="mx-auto mb-8" max-width="400">
          <v-img height="200px" :src="card.src"> </v-img>
          <v-card-title v-text="card.title"></v-card-title>
          <v-card-subtitle class="pb-0" v-text="card.subtitle">
          </v-card-subtitle>

          <v-card-text
            class="text--primary mt-3"
            style="white-space: pre-wrap"
            v-text="card.text"
          >
          </v-card-text>

          <v-card-actions>
            <v-btn
              v-if="card.link"
              color="rgb(116,166,76)"
              :href="card.link"
              target="_blank"
              text
            >
              VISIT
            </v-btn>
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
        title: '研究室紹介ページ',
        subtitle: 'STUDIOを利用して作成',
        src: require('../assets/ocimg.jpg'),
        text:
          'STUDIOでデザインを担当。レスポンシブに対応させる点で苦戦した。\nこの時、Webアプリ制作会社で実務経験のあるゼミの先輩に多くを学び、デザインだけでなく、自分もWebアプリケーションを実装してみたいと考えるようになる。',
        link: 'https://keita-lab.jp/OC2020',
      },
      {
        title: 'SkillUpChat',
        subtitle: 'Vue3, Firebase, を用いて制作',
        src: require('../assets/Skillupimg.png'),
        text:
          'モダンなWeb制作技術を学び、スキルアップするために初めて制作したアプリケーション。\nWeb技術を本格的に学習し始めて１ヶ月余りで作り上げた。',
        link: 'https://skillupchat.web.app/',
        xs: 12,
        sm: 12,
        md: 12,
        lg: 6,
        xl: 6,
      },

      {
        title: 'ポートフォリサイト',
        subtitle: 'Nuxt.js, Vuetify, Netlifyを用いて制作',
        src: require('../assets/Portfolioimg.png'),
        text:
          '静的サイトということでNuxt.jsのSSGを利用して実装。ホスティングはNetlifyで行った。\nレスポンシブデザインにも考慮して制作。',
        link: '',
        xs: 12,
        sm: 12,
        md: 12,
        lg: 6,
        xl: 6,
      },

      {
        title: 'Witty Game Console',
        subtitle: 'Vue3, TypeScriptを用いて鋭意製作中',
        src: require('../assets/WGC.jpg'),
        text:
          'もしも据え置き型ゲーム機にディスプレイがついてたら...\nこのアイデアを発端に様々な機能をVue3とTypeScriptを使用して実装していきます。',
        link: 'https://youtu.be/4WgxJo4LhEM',
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
