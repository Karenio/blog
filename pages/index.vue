<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <div class="text-center">
        <logo />
      </div>
      <div class="home text-center ma-10">
      <div class="text-h3">Rinruren</div>
      <div class="text-h5">凛流レン</div>

      <div class="text-h5 mt-15 mb-5 primary">Introduction</div>
      <p>はじめまして、Rinrerunです。<br>
      サイバーセキュリティと技術書執筆に興味があります。<br>
      執筆依頼・イベントなどの連絡はTwitterのDMにて受け付けています。<br>
      Twitter @rinruren</p>
      </div>
    </v-col>
  </v-row>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo,
  }
}
</script>
