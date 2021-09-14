<template>
  <v-app class="fubon-test">
    <v-img sizes="" src="@/assets/img/image_background.svg">
      <template v-slot:defaut>
        <div>
          <v-app-bar app color="agba(0,0,0,0)" fixed elevation="0">
            <v-container class="d-flex justify-space-between">
              <h1 class="font-weight-light">HOTEL</h1>
              <div>
                <v-btn
                  class="font-weight-thin"
                  text
                  v-for="n in menuList"
                  :key="n"
                >
                  {{ n }}
                </v-btn>
              </div>
              <v-btn width="170" height="48" outlined rounded color="white">
                SIGN UP
              </v-btn>
            </v-container>
          </v-app-bar>
        </div>
      </template>
    </v-img>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    menuList: ["About", "Service", "Rooms", "Blog", "Contact"],
  }),
};
</script>
<style lang="scss">
.fubon-test {
  font-family: adobe-heiti-std, sans-serif;
  font-weight: 400;
  font-style: normal;
}
h1 {
}
</style>
