<template lang="pug">
v-app(app)
  v-main(app)
    v-container(app)
      router-view
</template>

<script>


export default {
  name: "App",
  components: {  },
  mounted() {
    this.$vuetify.mode="dark"
  },
};
</script>
