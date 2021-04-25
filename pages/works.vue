<template>
  <div class="about text-center ma-10">
    <div class="text-h3">Works</div>
    <div class="text-h5 mt-15 mb-5 primary">Application</div>
    <div class="ma-10" v-for="(item, i) in app" :key="i">
    <v-card class="mx-auto my-12" max-width="400">
        <v-img height="100" :src="item.img"></v-img>
        <v-card-title>{{ item.name }}</v-card-title>
        <v-card-text>
            <div class="my-4 subtitle-1">{{ item.path }}</div>
            <div>{{ item.values }}</div>
        </v-card-text>
        <v-divider class="mx-4"></v-divider>
        <v-card-text>
        <v-chip-group
            active-class="white--text"
            color="primary"
            column
        >
            <v-chip color="primary">{{ item.chip1 }}</v-chip>
            <v-chip color="primary">{{ item.chip2 }}</v-chip>
        </v-chip-group>
        </v-card-text>
    </v-card>
    </div>
    <div class="text-h5 mt-15 mb-5 primary">Writing</div>
    <div class="ma-10" v-for="(item, i) in writing" :key="i">
    <v-card class="mx-auto my-12" max-width="400">
        <v-img height="100" :src="item.img"></v-img>
        <v-card-title>{{ item.name }}</v-card-title>
        <v-card-text>
            <div class="my-4 subtitle-1">{{ item.path }}</div>
            <div>{{ item.values }}</div>
        </v-card-text>
        <v-divider class="mx-4"></v-divider>
        <v-card-text>
        <v-chip-group
            active-class="white--text"
            color="primary"
            column
        >
            <v-chip color="primary">{{ item.chip1 }}</v-chip>
            <v-chip color="primary">{{ item.chip2 }}</v-chip>
        </v-chip-group>
        </v-card-text>
    </v-card>
    </div>
  </div>
</template>

<script>
export default {
  data() {
      return {
          app: [{
            img: require(".././assets/storyctf.png"),
            name: "StoryCTF",
            path: "https://storyctf.netlify.app",
            values: "ストーリー形式の初心者向けCTFです。",
            chip1: "Vue.js",
            chip2: "Netlify" 
          },],
          writing: [{
            img: require(".././assets/secshort.jpg"),
            name: "セキュリティショートショート",
            path: "https://techbookfest.org/product/5658972004548608?productVariantID=5508769347796992",
            values: "セキュリティに関する知識を、物語形式で広く浅く楽しく知ることを目的とした本です。",
            chip1: "技術書典",
            chip2: "セキュリティ" 
          },{
            img: require(".././assets/cover.png"),
            name: "SecHack365文芸部_部誌",
            path: "https://zenn.dev/sechack365books/books/department-magazine",
            values: "Zennで公開した、SecHack365文芸部員がテーマ「セキュリティ」で自由に書いた記事集です。",
            chip1: "Zenn",
            chip2: "セキュリティ" 
          },{
            img: require(".././assets/bungeibu.png"),
            name: "2020SecHack365文芸部部誌　年越し号",
            path: "https://techbookfest.org/product/5709819870707712?productVariantID=5162442529177600",
            values: "技術書典10に出典した、SecHack365文芸部員がテーマ「セキュリティ」で自由に書いた記事集です。",
            chip1: "技術書典",
            chip2: "セキュリティ" 
          },],
      };
  }
}
</script>