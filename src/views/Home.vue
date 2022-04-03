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
      span An application development method based on a model and its flow.
  v-row
    v-col(class="tw-flex items-center justify-center")
      v-btn(elevation="0" class="tw-mx-1" href="https://github.com/fookiejs/core" target="#") Github 
        v-icon(right) mdi-github
      v-btn(elevation="0" class="tw-mx-1" href="https://fookiejs.github.io/core/" target="#") Documentation 
        v-icon(right) mdi-book-outline
      v-btn(elevation="0" class="tw-mx-1" href="https://github.com/fookiejs/examples" target="#") Examples  
        v-icon(right) mdi-file-code-outline
  v-row(class=" tw-text-center")
    v-col
      span(class="tw-text-2xl") Tool & Plugins
  v-row(justify="tw-grid tw-grid-rows-4 tw-gap-4 justify-center")
    div(v-for="plugin in plugins")
      v-card(width="380")
        v-card-title {{ plugin.name }}
        v-card-subtitle {{ plugin.desc }}
        v-card-text
          v-chip(class="tw-font-italic" label)
            span(class="tw-text-green-600 tw-mr-2 tw-font-bold") {{">"}}
            span(class="tw-text-gray-900 tw-font-bold") {{plugin.npm}}
            
  v-row
    v-col
</template>

<script>
export default {
  data() {
    return {
      plugins: [
        {
          name: "Core",
          link: "https://github.com/fookiejs/cache",
          desc: "Fookie JS Core",
          npm: "npm install fookie",
        },
        {
          name: "Server",
          link: "https://github.com/fookiejs/cache",
          desc: "Allows the application to respond to http request.",
          npm: "npm install fookie-server",
        },
        {
          name: "Databases",
          link: "https://github.com/fookiejs/cache",
          desc: "Allows to use application with various databases.",
          npm: "npm install fookie-databases",
        },
        {
          name: "Cache",
          link: "https://github.com/fookiejs/cache",
          desc: "Solve cache needs in seconds.",
          npm: "npm install fookie-cache",
        },
        {
          name: "Cron",
          link: "https://github.com/fookiejs/cache",
          desc: "CronJob solution.",
          npm: "npm install fookie-cron",
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
code {
  font-family: monospace;
}
</style>
