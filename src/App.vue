<template>
  <v-app class="fubon-test">
    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'App',

  data: () => ({}),
}
</script>
<style lang="scss">
.fubon-test {
  font-family: adobe-heiti-std, sans-serif;
  font-weight: 400;
  font-style: normal;
}
</style>
