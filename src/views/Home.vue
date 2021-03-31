<template>
<v-container>
    <div class="mx-auto mt-6">
      <v-alert
        v-if="errorMessage"
        type="error"
      >
        <h5>{{ errorMessage }}</h5>
      </v-alert>
  <h1 class="py-12 green--text"> what ever could you meme? </h1>
  </div>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      errorMessage: null,
    };
  },
  mounted() {
    const hasAuthErr = this.$route.query.unauthorized === "true";
    if (hasAuthErr) {
      this.errorMessage = "You must be logged in to do that";
    }
  },
};
</script>

<style>
h1 {
text-align: center;
}
</style>