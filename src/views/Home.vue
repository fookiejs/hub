<template lang="pug">
div(class="tw-grid tw-gap-8")
  v-row
    v-col(class="tw-text-8xl tw-text-center tw-font-bold")
       span() The 
       span(class="grad") Revolutionary
       br
       span TypeScript Framework
  v-row
    v-col(class="tw-text-xl tw-text-center")
      span Design Once, Extend Infinitly
      br
      span Comprehensive model-based application development framework
  v-row
    v-col(class="tw-flex items-center justify-center")
      v-btn(elevation="0" class="tw-mx-1" href="https://github.com/fookiejs/core" target="#") Github 
        v-icon(right) mdi-github
      v-btn(elevation="0" class="tw-mx-1" href="https://fookiejs.github.io/core/" target="#") Documentation 
        v-icon(right) mdi-book-outline
      v-btn(elevation="0" class="tw-mx-1" href="https://github.com/fookiejs/examples" target="#") Examples  
        v-icon(right) mdi-file-code-outline
  v-row(class="tw-text-center")
    v-col
      span(class="tw-text-2xl") Ecosystem
  v-row(class="tw-grid tw-grid-cols-1 md:tw-grid-cols-3 lg:tw-grid-cols-4 tw-gap-4")
    div(v-for="repo in repos")
      v-card(outlined class="tw-w-full tw-flex tw-flex-col tw-justify-between tw-rounded-lg")
        div
          v-card-title(class="tw-text-xl tw-font-semibold")
            span {{repo.name}}
            v-spacer
            v-btn(:href="repo.html_url" target="#" icon)
              v-icon() mdi-link  
          v-card-subtitle(class="tw-text-sm") {{repo.description || "-"}}
          v-card-text
            v-chip(label outlined class="tw-mr-1") 
              v-icon(left small) mdi-star     
              span {{repo.stargazers_count}} 
            v-chip(label outlined) 
              v-icon(left small) mdi-eye     
              span {{repo.watchers}}
        v-card-actions(class="tw-p-4")
          v-chip(class="tw-mr-1" v-for="t in repo.topics" small dark) {{t}}


  v-row
    v-col
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      repos: [],
    };
  },
  mounted: async function () {
    let res = await axios.get("https://api.github.com/orgs/fookiejs/repos");
    console.log(res.data);
    this.repos = res.data;
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
