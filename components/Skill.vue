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
                  <v-chip>使用歴: {{ skill.years }}年</v-chip>
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
          name: 'C',
          description:
            'RTOS上で動作する組込みソフトウェアのコーディング経験があります',
          years: 8,
        },
        {
          name: 'Ruby',
          description:
            'Railsでの開発だけでなくmrubyのデバッガーの開発経験もあります',
          years: 2,
        },
        {
          name: 'HTML/CSS',
          description:
            'デザインテンプレートを使用してページをコーディングする程度です',
          years: 1,
        },
        {
          name: 'JavaScript',
          description: '業務では必要があれば書きます。最近は趣味でも書きます',
          years: 1,
        },
        {
          name: 'Go',
          description:
            '趣味のレベルではありますが動向をウォッチしている言語です',
          years: 1,
        },
      ],
    }
  },
}
</script>

<style></style>
