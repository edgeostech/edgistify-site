<template>
  <v-container fluid class="dark-store-main pa-0 ma-0">
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-row id="dark_store" no-gutters>
      <div class="main_title">
        <h1>Dark Store Operations</h1>
      </div>
    </v-row>
    <v-row class="main_content pa-0 ma-0">
      <v-col class="main_left_image pa-0 pb-12" sm="12" md="6">
        <v-img src="/Solutions/warehousing/dark-store-edgistify.jpg" contain />
      </v-col>
      <v-col class="main_right_content pa-0" sm="12" md="6">
        <div class="content-header">
          <h1>
            Enable Instant Delivery <br /> Everywhere You Sell
          </h1>
        </div>
        <div class="content-para">
          <p>
            Use our dark store network and delight your customers with super-fast deliveries and an unparalleled
            post-purchase experience that translates to increased sales and customer loyalty.
            Offer 30 min delivery to your customers using our minimal footprint and high-throughput solutions for picking,
            packing and dispatch.
          </p>
        </div>
        <div class="content-para-list">
          <div class="list">Minimal Picking Time</div>
          <div class="list">Expedited Order Delivery</div>
          <div class="list">Lower Operating Costs</div>
          <div class="list">Increased Efficiency</div>
        </div>
        <div class="content-button">
          <v-btn class="button bg-black" data-aos="fade-up" data-aos-once="true" data-aos-easing="ease-in"
            data-aos-anchor=".content-para" data-aos-duration="1000" @click="showModal = true">Schedule a call</v-btn>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import ConnectModal from "../../../ModalForm/ConnectModal.vue";

export default {
  components: {
    ConnectModal,
  },
  data () {
    return {
      showModal: false,
    };
  },
};
</script>
<style lang="scss" scoped>
.dark-store-main {
  width: 100%;
  height: auto;
  display: flex;
  flex-direction: column;

  .main_title {
    width: 100%;
    display: flex;
    background: #00a699;
    justify-content: baseline;
    align-items: center;
    padding: 0 6% !important;

    h1 {
      font-family: "Noto Serif";
      font-style: normal;
      font-weight: 400;
      font-size: 42px;
      line-height: 57px;
      color: #ffffff;
      padding: 12px;
    }
  }

  .main_content {
    display: flex;
    padding: 0 6% !important;
    background: #0c0c0c;

    .main_left_image {
      margin: 50px 0 0 0;
      padding-right: 58px !important;
    }

    .main_right_content {
      display: flex;
      flex-direction: column;
      margin: 50px 0 0 0;
      position: relative;

      .content-header {
        width: 100%;

        h1 {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 300;
          font-size: 32px;
          line-height: 44px;
          color: #ffffff;
        }
      }

      .content-para {
        width: 100%;
        margin-right: 1rem;
        height: auto;
        margin-top: 2rem;

        p {
          font-family: "Outfit";
          font-style: normal;
          font-weight: 300;
          font-size: 16px;
          line-height: 20px;
          color: #9c9c9c;
        }
      }

      .content-para-list {
        width: 100%;
        margin-top: 1rem;
        border-left: 1px solid #ffffff;
        transform: rotate(0deg);

        .list {
          font-family: "Outfit";
          font-style: normal;
          font-weight: 300;
          font-size: 16px;
          line-height: 24px;
          margin-left: 1rem;
          color: #ffffff;
        }
      }

      .content-button {
        margin-bottom: 48px;
        margin-top: 48px;
        position: absolute;
        bottom: 0;

        .button {
          display: flex;

          width: 11rem;
          height: 3rem;
          //border: 1px solid #00a699;
          border-radius: 73px;
          color: #fff;
          // padding: 0px 40px;
          text-transform: initial;
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 700;
          font-size: 18px;
          line-height: 25px;
          border: none;
          letter-spacing: 0px;
          //background:transparent;
          color: #ffffff;
          //padding:0 0 0 10px;
          // span {
          //    font-weight: 500 !important;
          // }

          &.primary {
            background-color: #00a699;
            box-shadow: inset 0 0 0 0 #00a699;
            transition: color 0.3s ease-in-out, box-shadow 0.3s ease-in-out;

            &:hover {
              box-shadow: inset 178px 0 0 0 #ffffff;
              color: #020202;
            }
          }
        }
      }
    }
  }
}

@media (max-width: 850px) {
  .dark-store-main .main_content .main_left_image {
    padding-right: 0 !important;
  }
  .main_title { 
    h1 {
      font-size: 30px !important
    }
  }
  .content-header {
    h1 {
      font-size: 24px !important;
      line-height: 30px !important;
    }
  }
  .main_right_content {
    margin: 0 !important;
  }
 
  .main_content {
    flex-wrap: wrap;
    height: auto !important;

    .main_left_image,
    .main_right_content {
      .content-para {
        margin-top: 30px !important;
        height: auto !important;
      }

      .content-header {
        height: auto !important;
      }

      .content-button {
        margin: 48px auto !important;
        position: unset !important;

      }
    }
  }
}
</style>
