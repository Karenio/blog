<template>
  <div class="about text-center ma-10">
    <div class="text-h3">About</div>
    <div class="text-h5 mt-15 mb-5 primary">profile</div>
    <div class="ma-10" v-for="(item, i) in profile" :key="i">
      <div class="text-h5 mb-3">{{ item.name }}</div>
      <div class="text-p">{{ item.values }}</div>
    </div>

    <div class="text-h5 mt-15 mb-5 primary">skills</div>
    <div class="text-h5 mb-3">Language</div>
    <div class="text-p">C++ JavaScript Python Kotlin Ruby Dart</div>
    <div class="text-h5 mb-3 mt-10">Framework</div>
    <div class="text-p">Vue.js React ReactNative Android Flutter</div>
    <div class="text-h5 mb-3 mt-10">Others</div>
    <div class="text-p">Writing Git GigHub VSCode AWS Netlify</div>
    <div class="text-h5 mb-3 mt-10">Qualification</div>
    <div class="text-p">剣道三段 漢検二級</div>

    <div class="text-h5 mt-15 mb-5 primary">Activities</div>
    
    <v-timeline
    align-top
    :dense="$vuetify.breakpoint.smAndDown"
  >
    <v-timeline-item
      v-for="(item, i) in items"
      :key="i"
      :color="item.color"
      :icon="item.icon"
      fill-dot
    >
      <v-card
        :color="item.color"
        dark
      >
        <v-card-title class="title">
          {{ item.name }}
        </v-card-title>
        <v-card-text class="white text--primary">
          <p class="black--text pt-7"> {{ item.values }}</p>
        </v-card-text>
      </v-card>
    </v-timeline-item>
  </v-timeline>
  </div>
</template>

<script>
export default {
  data() {
      return {
          profile: [{
            name:"Name",
            values:"Rinruren"
          },{
            name:"Age",
            values:"18"
          },{
            name:"Likes",
            values:"books & security"
          }],
          items: [{
            color: 'primary',
            icon: 'mdi-star',
            name: "2018.4 高専入学",
            values: "とある高専に推薦入試で入学"
          },{
            color: 'primary',
            icon: 'mdi-star',
            name: "2018.7 第53回全国高等専門学校体育大会剣道競技 東海地区体育大会",
            values: "個人・女子団体ともに優勝"
          },{
            color: 'primary',
            icon: 'mdi-star',
            name: "2018.8 第53回全国高等専門学校体育大会剣道競技 全国大会",
            values: "女子団体優勝"
          },{
            color: 'accent',
            icon: 'mdi-star',
            name: "2019.8 日本漢字能力検定",
            values: "漢検二級合格"
          },{
            color: 'accent',
            icon: 'mdi-star',
            name: "2019.9 剣道昇段審査会",
            values: "剣道三段合格"
          },{
            color: 'primary',
            icon: 'mdi-star',
            name: "2020.6 未来ドラフト2020",
            values: "グランプリ受賞"
          },{
            color: 'primary',
            icon: 'mdi-star',
            name: "2020.3 SecHack365 学習駆動コース コンテンツゼミ",
            values: "修了"
          },],
      };
  },
}
</script>