<template lang="pug">
v-app(app)
  v-app-bar(app)
    v-container
      v-row(align="center")
        v-toolbar-title Fookie JS
        v-spacer
        v-btn(text) Doc
        v-btn(icon)
          v-icon mdi-discord
  v-main(app)
    v-container(app)
      router-view
</template>

<script>
export default {
  name: "App",
  components: {},
  mounted() {},
};
</script>
