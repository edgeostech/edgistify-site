<template>
  <v-container fluid class="our-network-container pa-0">
    <v-col cols="12" class="heading pt-9 pb-9">
      <h2
        data-aos="fade-up"
        data-aos-once="true"
        data-aos-easing="ease-in"
        data-aos-duration="800"
      >
        Catering to a Wide Spectrum of Industries
      </h2>
    </v-col>
    <v-row class="cards-container pt-3 pb-9 pt-0">
      <v-col cols="4" sm="4" md="3" class="pr-md-6 pb-6">
        <div
          class="card ml-0"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="800"
        >
          <div class="icon-container food-bvgs"></div>
          <div class="title-text">Food and Beverages</div>
        </div>
      </v-col>
      <v-col cols="4" sm="4" md="3" class="px-md-6 pb-6">
        <div
          class="card ml-0"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="800"
        >
          <div class="icon-container fruits-vegetables"></div>
          <div class="title-text">Fruits and Vegetables</div>
        </div>
      </v-col>
      <v-col cols="4" sm="4" md="3" class="px-md-6 pb-6">
        <div
          class="card ml-0"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="800"
        >
          <div class="icon-container health-wellness"></div>
          <div class="title-text">Health and Wellness</div>
        </div>
      </v-col>
      <v-col cols="4" sm="4" md="3" class="pl-md-6 pb-6">
        <div
          class="card ml-0"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="800"
        >
          <div class="icon-container pharma"></div>
          <div class="title-text">Pharma</div>
        </div>
      </v-col>
      <!-- </v-col> -->
      <!-- <v-col cols="12" class="cards-container" data-aos="fade-up" data-aos-once="true" data-aos-easing="ease-in"
      data-aos-duration="800"> -->
      <v-col cols="4" sm="4" md="3" class="pr-md-6 pb-6">
        <div
          class="card ml-0"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="800"
        >
          <div class="icon-container d2c"></div>
          <div class="title-text">D2C</div>
        </div>
      </v-col>
      <v-col cols="4" sm="4" md="3" class="px-md-6 pb-6">
        <div
          class="card ml-0"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="800"
        >
          <div class="icon-container e-commerce"></div>
          <div class="title-text">Ecommerce</div>
        </div>
      </v-col>
      <v-col cols="4" sm="4" md="3" class="px-md-6 pb-6">
        <div
          class="card ml-0"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="800"
        >
          <div class="icon-container home-furnishing"></div>
          <div class="title-text">Home and Living</div>
        </div>
      </v-col>
      <v-col cols="4" sm="4" md="3" class="pl-md-6 pb-6">
        <div
          class="card ml-0"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="800"
        >
          <div class="icon-container industrials"></div>
          <div class="title-text">Industrials</div>
        </div>
      </v-col>
      <v-col cols="4" sm="4" md="3" class="pr-md-6 pb-6">
        <div
          class="card ml-0"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="800"
        >
          <div class="icon-container fmcg"></div>
          <div class="title-text">FMCG</div>
        </div>
      </v-col>
      <v-col cols="4" sm="4" md="3" class="px-md-6 pb-6">
        <div
          class="card ml-0"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="800"
        >
          <div class="icon-container beauty-lifestyle"></div>
          <div class="title-text">Cosmetics and Personal Care</div>
        </div>
      </v-col>
      <v-col cols="4" sm="4" md="3" class="px-md-6 pb-6">
        <div
          class="card ml-0"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="800"
        >
          <div class="icon-container consumer-goods"></div>
          <div class="title-text">Consumer Goods</div>
        </div>
      </v-col>
      <v-col cols="4" sm="4" md="3" class="pl-md-6 pb-6">
        <div
          class="card ml-0"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="800"
        >
          <div class="icon-container automative"></div>
          <div class="title-text">Automotive</div>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<style lang="scss" scoped>
@media (max-width: 850px) {
  .our-network-container {
    height: auto !important;

    // padding: 0 20px !important;
    .heading {
      h2 {
        font-size: 24px !important;
        line-height: 30px !important;
      }
    }
  }

  .cards-container {
    flex-wrap: wrap !important;
    height: auto !important;

    .card {
      // flex: 1 0 33.33%;
      // margin: 5px;
      // width: 5.978rem !important;
      height: 8rem !important;
      display: flex;
      align-items: center;
      justify-content: center;

      .icon-container {
        width: 100% !important;
        height: 50% !important;
        background-size: 40% !important;
      }

      .title-text {
        height: auto !important;
        width: 100% !important;
        font-family: "Outfit" !important;
        font-style: normal !important;
        font-weight: 400 !important;
        font-size: 0.75rem !important;
        line-height: 1rem;
      }
    }
  }
}

.our-network-container {
  height: auto;
  background-color: #fff;

  .heading {
    height: auto;
    padding: 0 6%;

    h2 {
      color: #1e1e1e;
      font-family: "Noto Serif";
      font-size: 42px;
      line-height: 44px;
    }
  }

  .cards-container {
    display: flex;
    height: auto;
    padding: 0 6%;
    flex-wrap: wrap;
    // gap: 2%;

    .card {
      display: flex;
      height: 12.125rem;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      background-color: #f3f3f5;
      transition: all 0.5s ease-in-out;

      .icon-container {
        display: flex;
        align-items: center;
        justify-content: center;
        width: 100%;
        height: 50%;
        background-size: 20%;
        background-position: center;

        &.food-bvgs {
          background-image: url("/Homepage/OurNetwork/food-bvgs.png");
        }

        &.fruits-vegetables {
          background-image: url("/Homepage/OurNetwork/fruits-_-vegetables.png");
        }

        &.health-wellness {
          background-image: url("/Homepage/OurNetwork/health-wellness.png");
        }

        &.pharma {
          background-image: url("/Homepage/OurNetwork/pharma.png");
        }

        &.d2c {
          background-image: url("/Homepage/OurNetwork/d2c.png");
        }

        &.e-commerce {
          background-image: url("/Homepage/OurNetwork/e-commerce.png");
        }

        &.home-furnishing {
          background-image: url("/Homepage/OurNetwork/home-furnishing.png");
        }

        &.industrials {
          background-image: url("/Homepage/OurNetwork/industrials.png");
        }

        &.fmcg {
          background-image: url("/Homepage/OurNetwork/fmcg.png");
        }

        &.beauty-lifestyle {
          background-image: url("/Homepage/OurNetwork/beauty-_-lifestyle.png");
        }

        &.consumer-goods {
          background-image: url("/Homepage/OurNetwork/consumer-goods.png");
        }

        &.automative {
          background-image: url("/Homepage/OurNetwork/automative.png");
        }
      }

      .title-text {
        display: flex;
        align-items: center;
        justify-content: center;
        text-align: center;
        font-weight: 500;
        font-family: "Outfit" !important;
        font-style: normal;
        font-size: 1rem;
        color: #000000;
      }

      &:hover {
        background-color: #000;

        .icon-container {
          &.food-bvgs {
            background-image: url("/Homepage/OurNetwork/food-bvgs-dark.png");
          }

          &.fruits-vegetables {
            background-image: url("/Homepage/OurNetwork/fruits-_-vegetables-dark.png");
          }

          &.health-wellness {
            background-image: url("/Homepage/OurNetwork/health-wellness-dark.png");
          }

          &.pharma {
            background-image: url("/Homepage/OurNetwork/pharma-dark.png");
          }

          &.d2c {
            background-image: url("/Homepage/OurNetwork/d2c-dark.png");
          }

          &.e-commerce {
            background-image: url("/Homepage/OurNetwork/e-commerce-dark.png");
          }

          &.home-furnishing {
            background-image: url("/Homepage/OurNetwork/home-furnishing-dark.png");
          }

          &.industrials {
            background-image: url("/Homepage/OurNetwork/industrials-dark.png");
          }

          &.fmcg {
            background-image: url("/Homepage/OurNetwork/fmcg-dark.png");
          }

          &.beauty-lifestyle {
            background-image: url("/Homepage/OurNetwork/beauty-_-lifestyle-dark.png");
          }

          &.consumer-goods {
            background-image: url("/Homepage/OurNetwork/consumer-goods-dark.png");
          }

          &.automative {
            background-image: url("/Homepage/OurNetwork/automative-dark.png");
          }
        }

        .title-text {
          color: #00a699;
        }
      }
    }
  }
}
</style>

<script>
import aosMixin from "~/mixins/aos";
export default {
  data() {
    return {
      selected: "Sectors",
    };
  },
  mixins: [aosMixin],
  methods: {
    toggleSelection(section) {
      if (this.selected !== section) this.selected = section;
    },
  },
};
</script>
