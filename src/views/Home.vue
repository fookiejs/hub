<template lang="pug">
div(class="tw-grid tw-gap-8")
  v-row
    v-col(class="tw-text-8xl tw-text-center tw-font-bold")
       span() The 
       span(class="grad") Revolutionary
       br
       span JavaScript Framework
  v-row
    v-col(class="tw-text-xl tw-text-center tw-text-gray-600")
      span Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed nisl est, consequat sit amet ultrices quis, congue non libero. 
  v-row
    v-col(class="tw-flex items-center justify-center")
      v-btn(text) Github 
        v-icon(right) mdi-github
      v-btn(text) Documentation 
        v-icon(right) mdi-file-document-multiple-outline
      v-btn(text) Examples 
        v-icon(right) mdi-file-code-outline

  v-row(class="tw-text-2xl tw-text-center")
    v-col
      h3 Plugins
  v-row(justify="tw-grid tw-gap-4 items-center justify-center")
    div(v-for="plugin in plugins")
      v-hover(v-slot="{ hover }")
        v-card( :dark="hover" :class="hover ? 'tw-cursor-pointer' : ''"  width="350")
          v-card-title {{ plugin.name }}
          v-card-text {{ plugin.desc }}
          v-card-text
            v-chip(small, dark) v{{ plugin.version }}
  v-row
    v-col
  v-row(class="tw-text-2xl tw-text-center")
    v-col
      span Utils
  v-row(justify="tw-grid tw-gap-4 items-center justify-center")
    div(v-for="util in utils")
      v-hover(v-slot="{ hover }")
        v-card(  :dark="hover" :class="hover ? 'tw-cursor-pointer' : ''"  width="350")
          v-card-title {{ util.name }}
          v-card-text {{ util.desc }}
          v-card-text
            v-chip(small, dark) v{{ util.version }}
</template>

<script>
export default {
  data() {
    return {
      plugins: [
        {
          name: "Server",
          link: "https://github.com/fookiejs/cache",
          desc: "Boktan açıklama burada.",
          version: "1.5.4",
        },
        {
          name: "Server",
          link: "https://github.com/fookiejs/cache",
          desc: "Boktan açıklama burada.",
          version: "1.5.4",
        },
        {
          name: "Server",
          link: "https://github.com/fookiejs/cache",
          desc: "Boktan açıklama burada.",
          version: "1.5.4",
        },
        {
          name: "Cache",
          link: "https://github.com/fookiejs/cache",
          desc: "Boktan açıklama burada.",
          version: "1.5.4",
        },
        {
          name: "Balancer",
          link: "https://github.com/fookiejs/cache",
          desc: "Boktan açıklama burada.",
          version: "1.5.4",
        },
      ],
      utils: [
        {
          name: "FOOKIE UI",
          link: "google.com",
          desc: "12312312",
          version: "1.5.4",
        },
      ],
    };
  },
};
</script>

<style>
.grad {
  background: -webkit-linear-gradient(red, darkred);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
</style>
