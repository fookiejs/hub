<template lang="pug">
div
  v-row
    v-col
      .tw-text-8xl The Revolutionary
      .tw-text-8xl JavaScript Framework
  v-row
    v-col
      h3 Plugins
      v-divider
  v-row(justify="space-center")
    v-card(v-for="plugin in plugins", width="350")
      v-card-title {{ plugin.name }}
      v-card-text {{ plugin.desc }}
      v-card-text
        v-chip(small, dark) v{{ plugin.version }}
  v-row
    v-col
  v-row 
    v-col
      h3 Utils
      v-divider
  v-row(justify="space-center")
    v-card(v-for="util in utils", width="350")
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
