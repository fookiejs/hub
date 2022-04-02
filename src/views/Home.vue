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
      v-btn(elevation="0" class="tw-mx-1" href="https://github.com/fookiejs/core" target="#") Github 
        v-icon(right) mdi-github
      v-btn(elevation="0" class="tw-mx-1" href="https://fookiejs.github.io/core/" target="#") Documentation 
        v-icon(right) mdi-book-outline
      v-btn(elevation="0" class="tw-mx-1" href="https://github.com/fookiejs/examples" target="#") Examples  
        v-icon(right) mdi-file-code-outline

  v-row(class="tw-text-2xl tw-text-center")
    v-col
      h3 Offical Plugins
  v-row(justify="tw-grid tw-gap-4 items-center justify-center")
    div(v-for="plugin in plugins")
      v-card(width="350")
        v-card-title {{ plugin.name }}
        v-card-text {{ plugin.desc }}
        v-card-text
          v-chip(small, dark) {{ plugin.version }}
  v-row
    v-col
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
          version: "v1.5.4",
        },
        {
          name: "Databases",
          link: "https://github.com/fookiejs/cache",
          desc: "Boktan açıklama burada.",
          version: "v1.5.4",
        },
        {
          name: "Cache",
          link: "https://github.com/fookiejs/cache",
          desc: "Boktan açıklama burada.",
          version: "v1.5.4",
        },
        {
          name: "Balancer",
          link: "https://github.com/fookiejs/cache",
          desc: "Boktan açıklama burada.",
          version: "In Progress",
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
