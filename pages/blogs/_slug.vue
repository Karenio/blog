<template>
  <v-row justify="center" align="center" class="background">
    <v-col cols="12" sm="10" md="9" class="col-center">
      <article>
        <div class="py-3">
          {{ blogs.date }}
          <h1>{{ blogs.title }}</h1>
          <div class="pb-3">
          <!--<tag-tip
            v-for="tag in article.tags"
            :key="tag"
            class="my-1 mr-2"
            :tag="tag"
          ></tag-tip>-->
          </div>
          <nuxt-content :document="blogs" />
        </div>
      </article>
    </v-col>
  </v-row>
</template>

<script>
export default {
 async asyncData ({ $content, params }) {
   const blogs = await $content('blogs', params.slug || 'index').fetch()
   return { blogs }
 }
}
</script>
