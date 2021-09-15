<template>
  <div>
    <div class="header">
      <v-container>
        <div class="d-flex justify-space-between">
          <h1 class="h-title white--text">HOTEL</h1>
          <div>
            <v-btn
              class="font-weight-thin white--text"
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
        </div>
        <div class="header-body">
          <h2>Exclusive Boutique Hotel</h2>
          <p>Luxury Boutique Hotel</p>
          <div>
            <img src="../assets/img/image_FB.svg" alt="" />
            <!-- <v-btn v-for="n in community" :key="`community-${n.alt}`">
              <img :src="n.img" :alt="n.alt" />
            </v-btn> -->
          </div>
        </div>
      </v-container>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      menuList: ["About", "Service", "Rooms", "Blog", "Contact"],
      // community: [
      //   {
      //     img: require(`@/assets/img/image_FB.svg`),
      //     alt: "icon-FB",
      //   },
      //   {
      //     img: require(`@/assets/img/image_twitter.svg`),
      //     alt: "icon-twitter",
      //   },
      //   {
      //     img: require(`@/assets/img/image_ig.svg`),
      //     alt: "icon-ig",
      //   },
      // ],
    };
  },
};
</script>
<style lang="scss">
@import "../assets/scss/mixin.scss";
.header {
  background-image: url("../assets/img/image_background.svg");
  background-size: cover;
  height: 500px;
  .h-title {
    font-size: 40px;
    font-weight: 400;
  }
  .header-body {
  }
}
</style>
