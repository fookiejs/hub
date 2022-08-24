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
  v-row(class="tw-text-center")
    v-col
      span(class="tw-text-2xl") Ecosystem
  v-row(class="tw-gap-4 justify-center")
    div(v-for="repo in repos")
      v-card(width="380" outlined)
        v-card-title {{repo.name}}
          v-spacer
          v-btn(:href="repo.html_url" target="#" icon)
            v-icon() mdi-link  
        v-card-subtitle {{repo.description || "-"}}
        v-card-text
          v-chip(label outlined class="tw-mr-1") 
            v-icon(left small) mdi-star     
            span {{repo.stargazers_count}} 
          v-chip(label outlined) 
            v-icon(left small) mdi-eye     
            span {{repo.watchers}}   
        v-card-actions
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
