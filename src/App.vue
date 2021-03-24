<template>
  <v-app>
    <v-app-bar app color="green lighten-3" dark>
      <router-link to="/">
  <v-btn text> Vue Meme Forum </v-btn>
</router-link>
  <v-spacer></v-spacer>
  <router-link to="/create">
  <v-btn text> Create </v-btn>
</router-link>
|
<router-link to="/feed">
  <v-btn text> Memes </v-btn>
</router-link>
</v-app-bar>

    <v-main>
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
export default {};
</script>

<style scoped>
a {
  text-decoration: none;
}
.router-link-active .v-btn {
  color: green;
}
</style>