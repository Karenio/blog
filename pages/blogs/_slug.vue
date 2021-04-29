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
          <div class="button">
            <a href="../blogs">
            <v-btn color="primary" elevation="24" large>一覧に戻る</v-btn>
            </a>
          </div>
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

<style lang="scss">
.button{
  padding: 100px 0px 0px 0px;
  text-align: center;
}
article {
  background-color: white;
  color: black;
  padding: 50px;
}
.nuxt-content {
  font-size: 1.05rem;
  h1 {
    border-bottom: solid 2px;
    border-bottom-color: primary;
    padding-top: 1.5rem;
    margin-bottom: 1.5rem;
    code {
      font-size: var(--font-size-h1);
    }
  }
  h2 {
    font-size: var(--font-size-h2);
    border-bottom: solid 2px;
    border-bottom-color: primary;
    padding-top: 1.0rem;
    margin-bottom: 1.0rem;
    code {
      font-size: var(--font-size-h2);
    }
  }
  h3 {
    font-size: var(--font-size-h3);
    padding-top: 0.5rem;
    margin-bottom: 0.5rem;
    code {
      font-size: var(--font-size-h3);
    }
  }
  h4 {
    font-size: var(--font-size-h4);
    padding-top: 0.5rem;
    margin-bottom: 0.5rem;
    code {
      font-size: var(--font-size-h4);
    }
  }
  h5 {
    font-size: var(--font-size-h5);
    code {
      font-size: var(--font-size-h5);
    }
  }
  p {
    font-size: 1.0rem;
  }
  code {
    font-size: 0.9rem !important;
    font-weight: 500 !important;
    font-family: Menlo,Monaco,Consolas,"Liberation Mono","Courier New",monospace !important;
  }
  ol {
    counter-reset: counter-name;
    li {
      margin: 0; 
      list-style: none;
    }
    li:before {
      counter-increment: counter-name;
      content: counter(counter-name) ".";
      position: absolute;
      left: 0;
      font-weight: bold;
    }
  }
  hr {
    border-top: 2px solid primary;
    margin-top: 0.5rem;
    margin-bottom: 0.5rem;
  }
  img {
    margin-top: 1.0rem;
    margin-bottom: 1.5rem;
  }
  blockquote {
    color: #777;
    padding-left: 1rem;
    border-left: solid 5px #C3CEE3;
  }
}
</style>