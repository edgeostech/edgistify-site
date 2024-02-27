<template>
  <v-container fluid class="dtoc-main pa-0">
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-row id="dtoc" class="main_content" no-gutters>
      <v-col class="main_left_image pa-0 pr-md-6 pb-6" md="6" sm="12">
        <div class="main_title">
          <h1>Direct-to-Consumer</h1>
        </div>
        <v-img src="/Solutions/sameday/dtoc-banner.png" contain />
      </v-col>
      <v-col class="main_right_content pa-0 pl-md-6 pt-12 pb-6" md="6" sm="12">
        <div class="content-header">
          <h1>Win Customers with Unmatched <br />Delivery Experience</h1>
        </div>
        <!-- <v-img
          src="/Solutions/sameday/dtoc-banner.png"
          contain
          v-if="isSmalldevice"
        /> -->
        <div class="content-para">
          <p>
            It takes work to acquire a customer. Delivering their purchase on
            the same day ensures those customers keep coming back. Same Day
            Delivery boosts your conversion rates and increases customer
            lifetime value. Our strategically built network of dark stores and
            warehouses, operational expertise and sophisticated technology
            allows you to deliver fast with zero errors. Same-day delivery
            reduces the cart drop rate by 20%, lessening the friction in your
            customers' purchase decisions.
          </p>
        </div>
        <div class="content-button">
          <v-btn
            class="button bg-white"
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="1000"
            @click="showModal = true"
            >Get in Touch</v-btn
          >
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
  data() {
    return {
      isSmalldevice: false,
      showModal: false,
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
.dtoc-main {
  background: #f3f3f5;

  .main_content {
    padding: 2% 6% !important;

    .main_left_image {
      .main_title {
        h1 {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 400;
          font-size: 42px;
          line-height: 57px;
          color: #0c0c0c;
        }
      }
    }

    .main_right_content {
      position: relative;

      .content-header {
        padding-top: 3%;
        h1 {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: normal;
          font-size: 32px;
          line-height: 44px;
          color: #1e1e1e;
        }
      }

      .content-para {
        width: 100%;
        padding-top: 2rem;

        p {
          font-family: "Outfit";
          font-style: normal;
          font-weight: 300;
          font-size: 16px;
          line-height: 20px;
          color: #313131;
        }
      }

      .content-button {
        position: absolute;
        bottom: 40px;

        .button {
          display: flex;
          height: 40px;
          width: 170px;
          border: 1px solid #00a699;
          border-radius: 73px;
          color: #fff;
          text-transform: initial;
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 700;
          font-size: 18px;
          line-height: 25px;
          color: #ffffff;

          span {
            font-weight: 500 !important;
          }

          &.primary {
            background-color: #00a699;
            box-shadow: inset 0 0 0 0 #00a699;
            transition: color 0.3s ease-in-out, box-shadow 0.3s ease-in-out;

            &:hover {
              box-shadow: inset 178px 0 0 0 #000000;
              color: #ffffff;
            }
          }
        }
      }
    }
  }
}

@media (max-width: 850px) {
  .dtoc-main {
    .main_content {
      padding: 3% 8% !important;

      .main_left_image {
        margin: 2% 0 0 0 !important;

        .main_title {
          h1 {
            font-family: "Noto Serif" !important;
            font-style: normal !important;
            font-weight: 400 !important;
            font-size: 30px !important;
            line-height: 3rem !important;
            color: #0c0c0c !important;
          }
        }
      }

      .main_right_content {
        padding-top: 0 !important;

        .content-header {
          h1 {
            font-family: "Noto Serif" !important;
            font-style: normal !important;
            font-weight: 300 !important;
            font-size: 24px !important;
            line-height: 30px !important;
            color: #1e1e1e !important;
          }
        }

        img {
          width: 100% !important;
          height: 100% !important;
        }

        .content-para {
          p {
            // padding-right: 24% !important;
            font-family: "Outfit" !important;
            font-style: normal !important;
            font-weight: 300 !important;
            font-size: 16px !important;
            line-height: 20px !important;
            color: #313131 !important;
          }
        }

        .content-button {
          position: unset !important;
          justify-content: center;
          display: flex;

          .button {
            height: 2.5rem !important;
            width: 9.188rem !important;
            border-radius: 3.75rem !important;
            padding: 0px 40px !important;
            font-family: "Noto Serif" !important;
            font-style: normal !important;
            font-size: 14px !important;
            line-height: 20px !important;
            font-weight: 300 !important;
          }
        }
      }
    }
  }
}
</style>
