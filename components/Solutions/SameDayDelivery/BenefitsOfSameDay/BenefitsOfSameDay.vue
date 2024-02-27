<template>
  <v-container fluid class="benefits-main pa-0">
    <v-row no-gutters class="pa-0" justify="space-between">
      <v-col cols="12" sm="12" md="3" class="pa-0">
        <div class="main-left">
          <div class="main_title">
            <h1>Benefits of Same Day Delivery</h1>
          </div>
        </div>
      </v-col>
      <v-col cols="12" sm="12" md="9" class="pa-0">
        <v-col cols="12" class="main-right pa-0">
          <v-col cols="12" class="cards-container pa-0">
            <v-col cols="6" sm="6" md="4" class="pr-md-6 pl-md-0 pb-6 pr-3 pb-md-12 pa-0">
              <div class="card">
                <div class="icon-container order-cancelleation"></div>
                <div class="title">
                  Reduction in Order <br />
                  Cancellations
                </div>
              </div>
            </v-col>
            <v-col cols="6" sm="6" md="4" class="px-md-6 pb-6 pl-2 pa-0 pb-md-12">
              <div class="card">
                <div class="icon-container customer-retention"></div>
                <div class="title">
                  Increased Customer <br />
                  Retention
                </div>
              </div>
            </v-col>
            <v-col cols="6" sm="6" md="4" class="pl-md-6 pr-md-0 pb-6 pr-3 pa-0 pb-md-12">
              <div class="card">
                <div class="icon-container competitive-advantage"></div>
                <div class="title">
                  Competitive <br />
                  Advantage
                </div>
              </div>
            </v-col>
            <!-- </v-col> -->
            <!-- <v-col class="cards-container pa-0"> -->
            <v-col cols="6" sm="6" md="4" class="pr-md-6 pl-md-0 pb-6 pl-2 pa-0 pb-md-12">
              <div class="card">
                <div class="icon-container improved-sales"></div>
                <div class="title">
                  Improved Sales <br />
                  and Revenue
                </div>
              </div>
            </v-col>
            <v-col cols="6" sm="6" md="4" class="px-md-6 pb-6 pr-3 pa-0 pb-md-12">
              <div class="card">
                <div class="icon-container hassle-free"></div>
                <div class="title">
                  Hassle-free<br />
                  Fulfillment
                </div>
              </div>
            </v-col>
            <v-col cols="6" sm="6" md="4" class="pl-3 pb-6 pa-0 pb-md-12">
              <div class="card">
                <div
                  class="icon-container delightful-customer-experience"
                ></div>
                <div class="title">
                  Delightful Customer<br />
                  Experience
                </div>
              </div>
            </v-col>
          </v-col>
        </v-col>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      isSmalldevice: false,
    };
  },
  mounted() {
    if (window.innerWidth <= 850) {
      this.isSmalldevice = true;
    } else {
      this.isSmalldevice = false;
    }
  },
};
</script>

<style lang="scss" scoped>


.benefits-main {
  width: 100%;
  display: flex;
  height: auto;
  background: white;
  padding: 0 6% !important;

  .main-left {
    width: 80%;
    height: auto;
    margin: 20% 0 0 0;

    .main_title {
      width: 100%;

      h1 {
        font-family: "Noto Serif";
        font-style: normal;
        font-weight: 400;
        font-size: 46.61px;
        line-height: 68px;
        color: #0c0c0c;
        padding-top: 0 !important;
      }
    }
  }

  .main-right {
    width: 100%;
    height: auto;
    margin: 7% 0 6% 0;
    // padding: 0 6% !important;

    .cards-container {
      justify-content: space-evenly;
      display: flex;
      align-items: center;
      flex-wrap: wrap;
      // padding: 10% 0;
      // gap: 10px;
      // width: 100%;
      height: auto;

      .card {
        display: flex;
        // width: 286px;
        height: 194px;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        background: #f3f3f5;

        .icon-container {
          display: flex;
          align-items: center;
          justify-content: center;
          width: 100%;
          height: 50%;
          background-size: 16%;
          background-position: center;

          &.order-cancelleation {
            background-image: url("/Solutions/sameday/order-cancellation.png");
          }

          &.customer-retention {
            background-image: url("/Solutions/sameday/customer-retention.png");
          }

          &.competitive-advantage {
            background-image: url("/Solutions/sameday/competitive-advantage.png");
          }

          &.improved-sales {
            background-image: url("/Solutions/sameday/improved-sales.png");
          }

          &.hassle-free {
            background-image: url("/Solutions/sameday/hassle-free.png");
          }

          &.delightful-customer-experience {
            background-image: url("/Solutions/sameday/delightful-customer-experience.png");
          }
        }

        .title {
          display: flex;
          text-align: center;
          align-items: center;
          justify-content: center;
          width: 100%;
          height: 30%;
          font-weight: 500;
          color: #000000;
          font-size: 16px !important;
          font-family: "Outfit" !important;
        }
      }
    }
  }
}

@media (max-width: 850px) {
  .benefits-main {
    flex-direction: column !important;
    height: auto !important;

    .main-left {
      width: 100% !important;
      height: auto !important;
      margin: 5% 0 0 0 !important;

      .main_title {
        width: 100% !important;

        h1 {
          font-family: "Noto Serif" !important;
          font-style: normal !important;
          font-weight: 400 !important;
          font-size: 2rem !important;
          line-height: 30px !important;
          color: #0c0c0c !important;
        }
      }
    }

    .main-right {
      width: 100% !important;
      height: auto !important;
      margin: 5% 0 0 0 !important;

      .cards-container {
        .card {
          // display: flex;
          // width: 30% !important;
          // height: 90% !important;
          height: 140px !important;
          // flex-direction: column;
          // align-items: center;
          // justify-content: center;

          .icon-container {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 100% !important;
            height: 50% !important;
            // background-size: 10% !important;
            background-position: center;
            background-size: auto;
          }

          .title {
            display: flex;
            text-align: center;
            align-items: center;
            justify-content: center;
            width: 100%;
            height: 40% !important;
            font-weight: 500;
            font-size: 12px !important;
            line-height: 1rem !important;
            color: #000000;
          }
        }
      }
    }
  }
}
</style>
