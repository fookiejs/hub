<template lang="pug">
div
  v-row
    v-col Fookie JS
  v-row
    v-col Desc
  v-row
    v-col Plugins
  v-row
    v-col(v-for="i in 6")
      v-card()
        v-card-title UI
  v-row 
    v-col Utils
  v-row
    v-col(v-for="i in 2")
      v-card()
        v-card-title UI
</template>

<script>
export default {
  data(){
    return {
      
    }
  }
};
</script>
