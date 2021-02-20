<template>
  <v-container fluid class="py-12 my-12">
    <v-row class="justify-center" no-gutters>
      <transition appear>
        <v-col cols="12">
          <div
            class="text-center mt-lg-4 mt-xl-4 text-subtitle-1 text-md-h6 text-lg-h6 text-xl-h5 font-weight-bold"
            style="color: rgb(116, 166, 76)"
          >
            Skills
          </div>
          <div
            class="text-center mb-10 text-h5 text-sm-h4 text-md-h3 text-lg-h3 text-xl-h2 font-weight-bold"
          >
            スキル
          </div>
        </v-col>
      </transition>
    </v-row>
    <v-row class="justify-center" no-gutters>
      <transition appear>
        <v-col cols="12">
          <v-row>
            <v-col v-for="skill in skills" :key="skill.name">
              <v-card>
                <v-card-title class="headline">
                  {{ skill.name }}
                </v-card-title>
                <v-card-text>
                  <v-chip>使用歴: {{ skill.long }}</v-chip>
                  <p>
                    {{ skill.description }}
                  </p>
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </v-col>
      </transition>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      skills: [
        {
          name: 'TypeScript',
          description: '現在研究に用いるためのwebページで使用中。',
          long: '2ヶ月',
        },
        {
          name: 'HTML/CSS/SCSS',
          description: 'レスポンシブ対応にも慣れてきた。',
          long: '1年',
        },
        {
          name: 'JavaScript',
          description: 'ES6以降の書き方も習得。',
          long: '1年',
        },
        {
          name: 'Vue',
          description:
            '簡単なアプリケーションを実装できる。CompositionAPIにも手を出し始める。',
          long: '3ヶ月',
        },
        {
          name: 'プロトタイピング',
          description:
            '素早くアイデアを具現化・検証し、フィードバックを経て実装。',
          long: '1年',
        },
        {
          name: 'PHP',
          description: 'Laravel鋭意勉強中',
          long: '2ヶ月',
        },
      ],
    }
  },
}
</script>

<style></style>
