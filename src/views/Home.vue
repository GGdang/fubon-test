<template>
  <div>
    <header class="header">
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
          <div class="sign-up-btn">
            <v-btn
              width="100%"
              height="100%"
              outlined
              rounded
              color="#FFFFFF4B"
            >
              <span class="white--text"> SIGN UP </span>
            </v-btn>
          </div>
        </div>
        <div class="header-body">
          <h2 class="b-title white--text">Exclusive Boutique Hotel</h2>
          <p class="b-sub-title white--text">Luxury Boutique Hotel</p>
          <div>
            <v-btn
              outlined
              fab
              v-for="n in community"
              :key="`community-${n.alt}`"
              width="48"
              height="48"
              class="mr-2"
            >
              <img :src="n.img" :alt="n.alt" />
            </v-btn>
          </div>
        </div>
        <v-row class="header-check-box white--text">
          <v-col
            class="d-flex pa-0 justify-space-between"
            cols="12"
            md="3"
            v-for="(n, key) in houseCheck"
            :key="key"
          >
            <div class="pt-7 pb-4 pl-8 pr-0">
              <p class="size-14">
                {{ key.toUpperCase() }}
              </p>
              <div class="d-flex align-center">
                <p class="mb-0 size-56">
                  {{ n.date }}
                </p>
                <div class="ml-5">
                  <div class="date-time">
                    <span class="size-18">{{ n.month }}</span>
                    <span class="size-18">
                      {{ n.year }}
                    </span>
                    <img
                      class="cursor-pointer ml-3"
                      src="../assets/img/button_onlyDropDown.svg"
                      alt="button_onlyDropDown"
                    />
                  </div>
                  <p class="mb-0 size-14">
                    {{ n.day }}
                  </p>
                </div>
              </div>
            </div>
            <v-divider color="#21364E" vertical></v-divider>
          </v-col>
          <v-col class="pa-0" cols="12" md="3">
            <div class="d-flex h-100">
              <div
                cols="6"
                class="people-box d-flex"
                v-for="(n, key) in people"
                :key="key"
              >
                <div class="pt-7 people-set d-flex align-center flex-column">
                  <p class="size-14">{{ key.toUpperCase() }}</p>
                  <div class="people-num">
                    <img
                      class="mr-4 cursor-pointer"
                      src="../assets/img/button_minus.svg"
                      alt="button_minus"
                    />
                    <span class="size-56">{{ n }}</span>
                    <img
                      class="ml-4 cursor-pointer"
                      src="../assets/img/button_plus.svg"
                      alt="button_plus"
                    />
                  </div>
                </div>
              </div>
            </div>
          </v-col>
          <v-col class="d-flex justify-center align-center" cols="12" md="3">
            <div class="check-btn">
              <v-btn width="100%" rounded height="100%" color="#C8FF8C">
                CHECK AVAILABILITY
              </v-btn>
            </div>
          </v-col>
          <img
            class="cursor-pointer"
            src="../assets/img/button_dropDown.svg"
            alt="button_dropDown"
          />
        </v-row>
      </v-container>
    </header>
    <main class="body">
      <v-container>
        <v-row no-gutters class="align-center">
          <v-col cols="6">
            <div class="size-56">
              <p class="mb-0 grey-1">Luxury Plaza</p>
              <p class="mb-0 grey-1">Hotel for You</p>
            </div>
            <div class="mt-2">
              <p class="mb-2 grey-2">
                Distant orb has power to raise and purify our
              </p>
              <p class="mb-2 grey-2">thoughts like a strain of sacred music.</p>
            </div>
            <v-btn
              class="mt-7"
              color="#333333"
              width="170"
              height="48"
              rounded
              outlined
            >
              ABOUT US
            </v-btn>
          </v-col>
          <v-col class="pa-0 hotel-vedio" cols="6">
            <img src="../assets/img/image_item.svg" alt="image_item" />
            <div class="vedio-play-box d-flex pa-8 align-center">
              <img
                class="mr-4 cursor-pointer"
                src="../assets/img/button_player.svg"
                alt="button_player"
              />
              <div>
                <p class="mb-3 grey-1">Play video</p>
                <p class="grey-2 mb-0">2:34</p>
              </div>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </main>
    <footer>
      <v-container>
        <v-row>
          <v-col cols="12" sm="12" md="9">
            <p class="white--text size-56 mb-0">HOTEL</p>
            <div class="d-flex flex-column flex-sm-row mt-7">
              <div
                class="
                  align-center
                  mr-0 mr-sm-7 mr-md-4 mr-lg-7
                  d-flex
                  mb-4 mb-sm-0
                "
                v-for="(n, key) in contact"
                :key="key"
              >
                <img class="mr-3" :src="n.img" :alt="`${key}-icon`" />
                <span
                  class="size-18"
                  :class="{
                    'white-2': key == 'position',
                    'white--text': key != 'position',
                  }"
                >
                  {{ n.content }}
                </span>
              </div>
            </div>
          </v-col>
          <v-col cols="12" sm="9" md="3">
            <p class="size-24 white--text">Subscribe</p>
            <input class="mb-3" placeholder="Email" type="text" />
            <p class="size-14 mb-0 white-2">No spam. Only profit.</p>
          </v-col>
        </v-row>
      </v-container>
    </footer>
  </div>
</template>
<script>
export default {
  name: "Home",
  data() {
    return {
      contact: {
        phone: {
          content: "(4321)0987-654-320",
          img: require("@/assets/img/Image_phone.svg"),
        },
        email: {
          content: "support@hotel.com",
          img: require("@/assets/img/Image_mail.svg"),
        },
        position: {
          content: "33 Jaja Park Rd, Yellow, USA",
          img: require("@/assets/img/Image_location.svg"),
        },
      },
      houseCheck: {
        arrival: {
          year: 2019,
          month: "Oct,",
          date: 18,
          day: "Friday",
        },
        departure: {
          year: 2019,
          month: "Oct,",
          date: 19,
          day: "Saturday",
        },
      },
      people: {
        adults: 2,
        children: 0,
      },
      menuList: ["About", "Service", "Rooms", "Blog", "Contact"],
      community: [
        {
          img: require(`@/assets/img/Image_FB.svg`),
          alt: "icon-FB",
        },
        {
          img: require(`@/assets/img/image_twitter.svg`),
          alt: "icon-twitter",
        },
        {
          img: require(`@/assets/img/Image_ig.svg`),
          alt: "icon-ig",
        },
      ],
    };
  },
};
</script>
<style lang="scss">
@import "../assets/scss/mixin.scss";
.grey-1 {
  color: #333333;
}
.grey-2 {
  color: #33333380;
}
.white-2 {
  color: #ffffff80;
}
.size-14 {
  font-size: 14px;
}
.size-18 {
  font-size: 18px;
}
.size-24 {
  font-size: 24px;
}
.size-56 {
  font-size: 56px;
}
.cursor-pointer {
  cursor: pointer;
}
.h-100 {
  height: 100%;
}
.header {
  background-image: url("../assets/img/image_background.svg");
  background-size: cover;
  .h-title {
    font-size: 40px;
    font-weight: 400;
  }
  .sign-up-btn {
    width: 170px;
    height: 48px;
  }
  .check-btn {
    width: 226px;
    height: 48px;
  }
  .header-body {
    margin-top: 156px;
    margin-bottom: 64px;
    .b-title {
      width: 329px;
      font-size: 72px;
      font-weight: 300;
      line-height: 80px;
      margin-bottom: 21px;
    }
    .b-sub-title {
      margin-bottom: 45px;
      font-size: 20px;
      font-weight: 300;
    }
  }
  .header-check-box {
    position: relative;
    background-color: #2c4664;
    box-shadow: 10px 10px 20px #00000019;
    border-radius: 15px;
    margin-bottom: 80px;
    .date-time {
      position: relative;
      img[alt="button_onlyDropDown"] {
        position: relative;
        top: 3px;
      }
    }
    img[alt="button_dropDown"] {
      position: absolute;
      left: 50%;
      bottom: -24px;
      transform: translateX(-50%);
    }
    .people-box {
      width: 50%;
      height: 100%;
      border-right: 1px #21364e solid;
      .people-set {
        width: 100%;
      }
      .people-num {
        position: relative;
        img[alt="button_minus"],
        img[alt="button_plus"] {
          position: relative;
          top: -24px;
        }
      }
    }
  }
}
.body {
  background-color: #edf1f5;
  padding-top: 144px;
  padding-bottom: 176px;
  .hotel-vedio {
    position: relative;
    height: 570px;
    overflow: hidden;
    border-radius: 30px;
    img[alt="image_item"] {
      height: auto;
      width: 100%;
    }
    .vedio-play-box {
      width: 100%;
      position: absolute;
      background-color: white;
      bottom: 0;
    }
  }
}
footer {
  padding-top: 95px;
  padding-bottom: 95px;
  background-color: #2c4664;
  @include dai_vuetify_md {
    padding-top: 90px;
    padding-bottom: 90px;
  }
  @include dai_vuetify_sm {
    padding-top: 75px;
    padding-bottom: 80px;
  }
  input[placeholder="Email"] {
    background-color: white;
    height: 48px;
    width: 100%;
  }
}
</style>
