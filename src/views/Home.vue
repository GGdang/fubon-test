<template>
  <div>
    <div class="header">
      <div>
        <v-container class="d-flex justify-space-between">
          <h1 class="font-weight-light">HOTEL</h1>
          <div>
            <v-btn class="font-weight-thin" text v-for="n in menuList" :key="n">
              {{ n }}
            </v-btn>
          </div>
          <v-btn width="170" height="48" outlined rounded color="white">
            SIGN UP
          </v-btn>
        </v-container>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {
      menuList: ['About', 'Service', 'Rooms', 'Blog', 'Contact'],
    }
  },
}
</script>
<style lang="scss">
.header {
  background-image: url('../assets/img/image_background.svg');
  height: 500px;
}
</style>
