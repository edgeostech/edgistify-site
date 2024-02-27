<template>
  <v-container fluid class="our-reach-container pa-0">
    <v-row no-gutters>
      <v-col cols="12" sm="12" md="6" class="left-section-container">
        <div class="heading-container">
          <h2 data-aos="fade-up" data-aos-once="true" data-aos-easing="ease-in" data-aos-duration="800" class="pb-6">
            Seamless Integrations
          </h2>
        </div>
        <div class="sub-heading-container">
          <span data-aos="fade-up" data-aos-once="true" data-aos-easing="ease-in" data-aos-duration="900">
            One-click integration with 50+ marketplaces, 20+ couriers and various ERPs. Efficiently manage and ship all
            orders
            on a single platform.
          </span>
        </div>
        <div class="brands-container pt-12">
          <v-row cols="12" md="12" sm="12" class="px-0" data-aos="fade-up" data-aos-once="true" data-aos-easing="ease-in"
            data-aos-duration="1000">
            <v-col cols="3" md="2" sm="3" class="brand">
              <v-img src="/Homepage/OurReach/amazon.png" class="img1" contain></v-img>
            </v-col>
            <v-col cols="3" md="2" sm="3" class="brand">
              <v-img src="/Homepage/OurReach/flipkart.png" class="img1" contain></v-img>
            </v-col>
            <v-col cols="3" md="2" sm="3" class="brand">
              <v-img src="/Homepage/OurReach/shopify.png" class="img1" contain></v-img>
            </v-col>
            <v-col cols="3" md="2" sm="3" class="brand">
              <v-img src="/Homepage/OurReach/meesho.png" class="img1" contain></v-img>
            </v-col>
            <v-col cols="3" md="2" sm="3" class="brand">
              <v-img src="/Homepage/OurReach/myntra.png" class="img1" contain></v-img>
            </v-col>
            <v-col cols="3" md="2" sm="3" class="brand">
              <v-img src="/Homepage/OurReach/cred.png" class="img1" contain></v-img>
            </v-col>
            <v-col cols="3" md="2" sm="3" class="brand">
              <v-img src="/Homepage/OurReach/woocommerce.png" class="img1" contain></v-img>
            </v-col>
            <v-col cols="3" md="2" sm="3" class="brand">
              <v-img src="/Homepage/OurReach/delhivery.png" class="img1" contain></v-img>
            </v-col>
            <v-col cols="3" md="2" sm="3" class="brand">
              <v-img src="/Homepage/OurReach/bluedart.png" class="img1" contain></v-img>
            </v-col>
            <v-col cols="3" md="2" sm="3" class="brand">
              <v-img src="/Homepage/OurReach/dtdc.png" class="img1" contain style="border-radius: 11px;"></v-img>
            </v-col>
            <v-col cols="3" md="2" sm="3" class="brand">
              <v-img src="/Homepage/OurReach/shiprocket.png" class="img1" contain></v-img>
            </v-col>
            <v-col cols="3" md="2" sm="3" class="brand">
              <v-img src="/Homepage/OurReach/shipsy.png" class="img1" contain></v-img>
            </v-col>
          </v-row>
        </div>
        <nuxt-link :to="{ path: '/solutions/tech-driven-supply-chain-and-warehouse-management-edgistify/', hash: '#automate-wrapper' }"
          style="text-decoration: none; color: inherit">
          <v-col class="view"> View all </v-col>
        </nuxt-link>
      </v-col>
      <v-col cols="12" sm="12" md="6" class="right-section-container">
      </v-col>
    </v-row>
  </v-container>
</template>
<style lang="scss" scoped>
.our-reach-container {
  display: flex;
  width: 100%;
  height: auto;
  background-color: #0c0c0c;
  padding-top: 20rem;
  // //background-image: url("/Common/background-grid.png");
  // background-position: bottom;
  // background-size: contain;

  .left-section-container {
    display: flex;
    // width: 50%;
    height: auto;
    flex-direction: column;
    justify-content: center;
    padding: 3% 6%;

    // border: 1px solid grey;
    .heading-container {
      display: flex;
      // width: 80%;
      height: auto;

      h2 {
        font-size: 42px;
        font-weight: 500;
        color: #fff;
        font-family: "Noto Serif";
      }
    }

    .sub-heading-container {
      display: flex;
      // width: 85%;
      height: auto;

      span {
        font-size: 1rem;
        font-weight: 300;
        color: #fff;
        font-family: "Outfit";
      }
    }

    .view {
      display: flex;
      justify-content: flex-end;
      // margin-top: 20px;

      font-family: "Outfit";
      font-style: normal;
      font-weight: 300;
      font-size: 1rem;
      line-height: 20px;
      color: #00a699;
      text-decoration: none;
    }

    .brands-container {
      // display: flex;
      // width: 100%;
      height: auto;
      // flex-direction: column;
      // align-items: center;
      // justify-content: space-between;

      .brands {
        display: flex;
        flex-wrap: wrap;

        height: auto;
        // width: 100%;
        align-items: center;
        justify-content: space-between;

        .brand {
          display: flex;
          align-items: center;
          justify-content: center;
          height: 5.313rem;
          width: 5.313rem;
          border-radius: 4px;

          .v-image {
            border-radius: 11px;
          }

          .img1 {
            width: 100%;
            height: 100%;
          }
        }
      }
    }
  }

  .right-section-container {
    height: auto;
    background-image: url("/Homepage/OurReach/hand.png");
    background-position: bottom;
    background-size: contain;
    .img {
      width: 200px;
      height: 200px;
      left: 21.5625rem;
      top: 0;
      opacity: 0.2;
      transition: all 0.8s ease;

      &:hover {
        opacity: 0.5;
      }
    }
  }
}

@media (max-width: 850px) {
  .our-reach-container {
    display: flex !important;
    width: 100% !important;
    height: auto !important;
    margin-top: 0px !important;
    align-items: center !important;
    flex-direction: column !important;
    padding-top: 5rem !important;

    .left-section-container {
      display: flex !important;
      width: 100% !important;
      // padding: 0 10% 0 10% !important;

      .heading-container {
        // display: flex !important;
        // width: 70% !important;
        height: auto !important;

        h2 {
          font-size: 26px !important;
          font-weight: 500 !important;
          line-height: 30px !important;
        }
      }

      .sub-heading-container {
        display: flex;
        // width: 95% !important;
        height: auto !important;

        span {
          font-size: 14px !important;
          font-weight: 300 !important;
          line-height: 20px !important;
        }
      }

      .brands-container {
        // width: 100% !important;
        display: flex !important;
        height: auto !important;
        justify-content: space-evenly !important;

        .brands {
          justify-content: space-between !important;

          .brand {
            justify-content: space-between !important;
            // width: 22% !important;
            height: auto !important;
            border-radius: 0.519rem !important;

            .img1 {
              width: 100% !important;
              height: 100% !important;
            }
          }
        }
      }

      .view {
        margin-top: 0px !important;
      }
    }

    .right-section-container {
      height: auto !important;
      padding-top: 55% !important;
      padding-left: 2rem !important;
      background-position: center !important;
      background-size: 40% !important;
      // background-position-y: 3.438rem !important;

      .img {
        width: 77.69px;
        height: 81.46px;
        top: -114px;
        left: 140px;
        opacity: 0.2;
        transition: all 0.8s ease;

        &:hover {
          opacity: 0.5;
        }
      }
    }
  }
}
</style>

<script>
import aosMixin from "~/mixins/aos";

export default {
  mixins: [aosMixin],
  data () {
    return {
      isSmallDevice: false,
    };
  },
  mounted () {
    if (window.innerWidth <= 850) {
      this.isSmallDevice = true;
    } else {
      this.isSmallDevice = false;
    }
  },
};
</script>
