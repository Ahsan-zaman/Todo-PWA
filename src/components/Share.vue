<template>
  <v-btn
    fixed
    dark
    fab
    right
    bottom
    color="#00848C"
    @click="share"
  >
    <v-icon>share</v-icon>
  </v-btn>
</template>

<script>
export default {
  methods: {
    async share() {
      console.log('clicked')
      try {
        await navigator.share({ title: "Todo PWA", url: "" });
        console.log("Data was shared successfully");
      } catch (err) {
        console.error("Share failed:", err.message);
      }
    }
  }
}
</script>

<style>
</style>
