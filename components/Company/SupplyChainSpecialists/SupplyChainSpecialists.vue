<template>
  <v-container fluid class="scm-main-container">
    <v-row class="scm-header" no-gutters>
      <h1 class="h1">Our Team</h1>
      <h1>Supply Chain Specialists</h1>
      <p>
        We are a founder-led team of supply chain experts on a mission to build
        a better tomorrow. Our passionate leadership team has a plentiful
        experience in fulfillment, warehousing and distribution.
      </p>
    </v-row>
    <v-row
      class="scm-wrapper my-md-16 fill-height"
      v-if="!isSmallDevice"
      justify="space-between"
      no-gutters
    >
      <v-col sm="12" md="4" class="scm-wrapper-row1 px-md-6" cols="4">
        <div class="specialists-details">
          <v-img
            :src="`/Company/edgistify-supply-chain-specialists-shubhajit-roy.jpg.jpg`"
            aspect-ratio="1"
            cover
            class="bg-grey-lighten-2"
          >
          </v-img>
          <div class="info-text">
            <h1>Shubhajit Roy</h1>
            <p>Entrepreneur In Residence</p>
          </div>
        </div>
      </v-col>
      <v-col sm="12" md="4" class="scm-wrapper-row1 px-md-6" cols="4">
        <div class="specialists-details">
          <v-img
            :src="`/Company/edgistify-supply-chain-specialists-sunil-bhatt.jpg.jpg`"
            alt="Sunil Bhatt heads the Solution design and Commercials at Edgistify"
            aspect-ratio="1"
            cover
            class="bg-grey-lighten-2"
          >
          </v-img>
          <div class="info-text">
            <h1>Sunil Bhatt</h1>
            <p>Head - Solutions Design and Commercial</p>
          </div>
        </div>
      </v-col>
      <v-col sm="12" md="4" class="scm-wrapper-row1 px-md-6" cols="4">
        <div class="specialists-details">
          <v-img
            :src="`/Company/edgistify-supply-chain-specialists-abhijit-kulkarni.jpg.jpg`"
            alt="Supply chain specialist and Procurement Head at Edgistify Abhijit Kulkarni managing the procurement process"
            aspect-ratio="1"
            cover
            class="bg-grey-lighten-2"
          >
          </v-img>
          <div class="info-text">
            <h1>Abhijit Kulkarni</h1>
            <p>AVP - Procurement</p>
          </div>
        </div>
      </v-col>
    </v-row>
    <v-row
      class="scm-wrapper my-md-16"
      v-if="!isSmallDevice"
      justify="space-between"
      no-gutters
    >
      <v-col sm="12" md="4" class="scm-wrapper-row1 px-md-6" cols="4">
        <div class="specialists-details">
          <v-img
            :src="`/Company/edgistify-supply-chain-specialists-tanveer-shaikh.jpg.jpg`"
            alt="Supply chain specialist and Operations leader at Edgistify Tanveer Shaikh managing the operations of key accounts"
            aspect-ratio="1"
            cover
            class="bg-grey-lighten-2"
          >
          </v-img>
          <div class="info-text">
            <h1>Tanveer Shaikh</h1>
            <p>AVP - Operations</p>
          </div>
        </div>
      </v-col>
      <v-col sm="12" md="4" class="scm-wrapper-row1 px-md-6" cols="4">
        <div class="specialists-details">
          <v-img
            :src="`/Company/edgistify-supply-chain-specialists-willieam-timothyy.jpg.jpg`"
            alt="Supply chain specialist and Operations Head at Edgistify Willieam Timothyy managing the operations of Clients on day to day basis"
            aspect-ratio="1"
            cover
            class="bg-grey-lighten-2"
          >
          </v-img>
          <div class="info-text">
            <h1>Willieam Timothyy</h1>
            <p>AVP - Operations</p>
          </div>
        </div>
      </v-col>
      <v-col sm="12" md="4" class="scm-wrapper-row1 px-md-6" cols="4">
        <div class="specialists-details">
          <v-img
            :src="`/Company/edgistify-supply-chain-specialists-saurabh-kumar.jpg.jpg`"
            alt="Saurabh Kumar handling the technology and product development in Edgistify"
            aspect-ratio="1"
            cover
            class="bg-grey-lighten-2"
          >
          </v-img>
          <div class="info-text">
            <h1>Saurabh Kumar</h1>
            <p>AVP - Tech and Product</p>
          </div>
        </div>
      </v-col>
    </v-row>
    <!-- Mobile Layout -->
    <v-row class="scm-wrapper" no-gutters v-if="isSmallDevice">
      <v-col sm="6" cols="6" class="pr-2 pb-2">
        <div class="specialists-details">
          <v-img
            :src="`/Company/edgistify-supply-chain-specialists-shubhajit-roy.jpg.jpg`"
            aspect-ratio="1"
            cover
            class="bg-grey-lighten-2"
          >
          </v-img>
          <div class="info-text">
            <h1>Shubhajit Roy</h1>
            <p>Entrepreneur In Residence</p>
          </div>
        </div>
      </v-col>
      <v-col sm="6" cols="6" class="pr-2 pb-2">
        <div class="specialists-details">
          <v-img
            :src="`/Company/edgistify-supply-chain-specialists-sunil-bhatt.jpg.jpg`"
            alt="Sunil Bhatt heads the Solution design and Commercials at Edgistify"
            aspect-ratio="1"
            cover
            class="bg-grey-lighten-2"
          >
          </v-img>
          <div class="info-text">
            <h1>Sunil Bhatt</h1>
            <p>Head - Solutions Design and Commercial</p>
          </div>
        </div>
      </v-col>
      <v-col sm="6" cols="6" class="pr-2 pb-2">
        <div class="specialists-details">
          <v-img
            :src="`/Company/edgistify-supply-chain-specialists-abhijit-kulkarni.jpg.jpg`"
            alt="Supply chain specialist and Procurement Head at Edgistify Abhijit Kulkarni managing the procurement process"
            aspect-ratio="1"
            cover
            class="bg-grey-lighten-2"
          ></v-img>
          <div class="info-text">
            <h1>Abhijit Kulkarni</h1>
            <p>AVP - Procurement</p>
          </div>
        </div>
      </v-col>
      <v-col sm="6" cols="6" class="pr-2 pb-2">
        <div class="specialists-details">
          <v-img
            :src="`/Company/edgistify-supply-chain-specialists-tanveer-shaikh.jpg.jpg`"
            alt="Supply chain specialist and Operations leader at Edgistify Tanveer Shaikh managing the operations of key accounts"
            aspect-ratio="1"
            cover
            class="bg-grey-lighten-2"
          >
          </v-img>
          <div class="info-text">
            <h1>Tanveer Shaikh</h1>
            <p>AVP - Operations</p>
          </div>
        </div>
      </v-col>
      <v-col sm="6" cols="6" class="pr-2 pb-2">
        <div class="specialists-details">
          <v-img
            :src="`/Company/edgistify-supply-chain-specialists-willieam-timothyy.jpg.jpg`"
            alt="Supply chain specialist and Operations Head at Edgistify Willieam Timothyy managing the operations of Clients on day to day basis"
            aspect-ratio="1"
            cover
            class="bg-grey-lighten-2"
          >
          </v-img>
          <div class="info-text">
            <h1>Willieam Timothyy</h1>
            <p>AVP - Operations</p>
          </div>
        </div>
      </v-col>
      <v-col sm="6" cols="6" class="pr-2 pb-2">
        <div class="specialists-details">
          <v-img
            :src="`/Company/edgistify-supply-chain-specialists-saurabh-kumar.jpg.jpg`"
            alt="Saurabh Kumar handling the technology and product development in Edgistify"
            aspect-ratio="1"
            cover
            class="bg-grey-lighten-2"
          >
          </v-img>
          <div class="info-text">
            <h1>Saurabh Kumar</h1>
            <p>AVP - Tech and Product</p>
          </div>
        </div>
      </v-col>
    </v-row>
    <!-- Mobile End -->
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      isSmallDevice: false,
    };
  },
  mounted() {
    if (window.innerWidth <= 850) {
      this.isSmallDevice = true;
    } else {
      this.isSmallDevice = false;
    }
  },
};
</script>

<style lang="scss" scoped>
.scm-main-container {
  width: 100%;
  background: #ffff;
  padding: 0 6% !important;

  .scm-wrapper-row1:first-child {
    margin-left: -24px;
  }
  .scm-wrapper-row1:last-child {
    margin-right: -24px;
  }
  .h1 {
    font-family: "Noto Serif";
    font-style: normal;
    font-weight: 500;
    font-size: 42px !important;
    line-height: 68px;
    color: #1a1a1a !important;
  }

  .scm-header {
    width: 100%;
    border-top: 1px solid #d9d9d9;
    display: flex;
    flex-direction: column;

    h1 {
      font-family: "Noto Serif";
      font-style: normal;
      font-weight: 500;
      font-size: 34px;
      line-height: 47px;
      color: #3c3c3c;
      padding-top: 2%;
    }

    p {
      font-family: "Outfit" !important;
      font-style: normal;
      font-weight: lighter;
      font-size: 16px;
      line-height: 20px;
      color: #5f5f5f;
      margin-top: 1.5rem;
    }
  }

  .scm-wrapper {
    width: 100%;
    height: auto;

    .specialists-details {
      .img {
        margin-bottom: 0.5rem;
      }

      .info-text {
        width: 100%;

        h1 {
          font-family: "Outfit";
          font-style: normal;
          font-weight: 500;
          font-size: 16px;
          line-height: 20px;
          color: #1a1a1a;
          margin-bottom: 0.25rem;
        }

        p {
          font-family: "Outfit";
          font-style: normal;
          font-weight: 300;
          font-size: 14px;
          line-height: 18px;
          color: #1a1a1a;
        }
      }
    }
  }
}

@media screen and (max-width: 850px) {
  .h1 {
    font-size: 30px !important;
  }
  .scm-main-container {
    width: 100%;
    height: auto !important;
    background: #ffff;
    // background: blueviolet;

    .scm-header {
      width: 100%;
      // margin: 0rem !important;
      display: flex !important;
      flex-direction: column !important;
      // padding: 2% 8% !important;

      h1 {
        padding-left: 0rem !important;
        font-family: "Noto Serif";
        font-style: normal;
        font-weight: 500;
        font-size: 24px !important;
        line-height: 30pxs !important;
        color: #1a1a1a;
      }

      .h1 {
    font-size: 30px !important;
  }
      p {
        padding-left: 0rem !important;
        width: 100% !important;
        font-size: 16px !important;
        line-height: 20px !important;
      }
    }

    .scm-wrapper {
      margin: 0rem !important;
      margin-bottom: 2rem !important;

      .specialists-details {
        .info-text {
          width: 100%;
          display: flex !important;
          flex-direction: column !important;
          align-items: flex-start !important;
          padding-top: 2px;

          h1 {
            font-size: 16px !important;
          }

          p {
            font-size: 14px !important;
          }
        }
      }
    }
  }
}
</style>
