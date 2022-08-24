<template lang="pug">
v-app(app)
  v-app-bar(app elevate-on-scroll)
    v-container
      v-row(align="center")
          v-app-bar-nav-icon 
            v-img(src="./assets/logo.png" max-height="32" contain)
          v-app-bar-title() Fookie.js
          v-spacer
          v-btn(text href="mailto:umut@fookiejs.com" target="#" )  Contact
            v-icon(right) mdi-email-outline
          v-btn(text href="https://discord.com/invite/Y4BPxTUMsh" target="#" ) Discord
            v-icon(right) mdi-account-group
          v-btn(text @click="dark = !dark") {{dark ? 'Light': 'Dark'}}
            v-icon(right) mdi-theme-light-dark
  v-main(app)
    v-container(app)
      router-view
  v-footer(padless)
    v-card(flat tile width="100%" class="tw-text-center")
      v-card-text
        | {{ new Date().getFullYear() }} &mdash; 
        strong Fookie JS

        

</template>

<script>
export default {
  name: "App",
  data() {
    return {
      dark: true,
    };
  },
  components: {},
  mounted() {
    this.$vuetify.theme.dark = true;
  },
  watch: {
    dark: function (val) {
      this.$vuetify.theme.dark = val;
    },
  },
};
</script>
