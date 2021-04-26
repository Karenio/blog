<template>
 <div>
   <div v-for="b in blogs" :key="b.slug">
       <v-card class="mx-auto my-12 white" max-width="800">
           <v-card-text>
           <nuxt-link :to="'/blogs/'+ b.slug">{{ b.date }}</nuxt-link>
           </v-card-text>
            <v-card-title>
                <nuxt-link :to="'/blogs/'+ b.slug">
                    {{ b.title }}
                </nuxt-link>
            </v-card-title>
       </v-card>
   </div>
 </div>
</template>

<script>
export default {
 async asyncData ({ $content, params }) {
   const query = await $content('blogs' || 'index').limit(10)
   const blogs = await query.fetch()
   return { blogs }
 }
}
</script>
