<template>
  <v-container fluid class="ecommerce-main pa-0">
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <div class="main_title">
      <h1>E-commerce</h1>
    </div>
    <v-row id="ecommerce" class="main_content" no-gutters>
      <v-col class="main_left_image pr-md-6 mb-12" sm="12" md="6">
        <div>
          <v-img
            src="/Solutions/sameday/ecommerce-banner.png"
            class="img"
            contain
          ></v-img>
        </div>
      </v-col>
      <v-col class="pl-6 main_right_content" sm="12" md="6">
        <div>
          <div class="content-header">
            <h1>Increase Repeat Orders By Building Customer Loyalty</h1>
          </div>

          <div class="content-para">
            <p>
              Accelerate your e-commerce business by quickly adapting to
              changing demands of your customers. Offer same-day delivery so
              that your customers don't look elsewhere. Expedite the journey of
              your products by promptly storing, picking, packing & delivering
              your orders through our Same Day Delivery network. Elevate your
              customers' delivery experience by providing real-time updates from
              placing the order to final delivery.
            </p>
          </div>
          <div class="content-button">
            <v-btn
              class="button bg-black"
              data-aos="fade-up"
              data-aos-once="true"
              data-aos-easing="ease-in"
              data-aos-duration="1000"
              @click="showModal = true"
              >Schedule a call</v-btn
            >
          </div>
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
.ecommerce-main {
  background: #0c0c0c;
  .main_title {
    width: 100%;

    h1 {
      font-family: "Noto Serif";
      font-style: normal;
      font-weight: 400;
      font-size: 42px;
      line-height: 57px;
      color: #ffffff;
      padding: 2% 6% 2% 6% !important;
    }
  }
  .main_content {
    padding: 0 6%;

    .main_left_image {
      width: 100%;
      display: flex;
      flex-direction: column;

      // img {
      //   padding-top: 2rem;
      //   width: 596px;
      //   height: 414px;
      // }
    }

    .main_right_content {
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
        padding-top: 2rem;

        p {
          font-family: "Outfit";
          font-style: normal;
          font-weight: 300;
          font-size: 16px;
          line-height: 20px;
          color: #9c9c9c;
        }
      }

      .content-button {
        display: flex;
        margin: 20px 0 0 0;
        position: absolute;

        bottom: 50px;

        .button {
          display: flex;
          height: 3rem;
          border: 1px solid #00a699;
          border-radius: 73px;
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 700;
          font-size: 18px;
          line-height: 25px;
          text-transform: capitalize;
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
  .ecommerce-main {
    background: #0c0c0c;

    .main_title {
      width: 100%;

      h1 {
        font-family: "Noto Serif" !important;
        font-style: normal !important;
        font-weight: 400 !important;
        font-size: 30px !important;
        line-height: 3rem !important;
        padding: 5% 6% 5% 6% !important;
      }
    }
    .main_content {
      .main_left_image {
        width: 100% !important;
        flex-direction: column !important;
      }

      .main_right_content {
        width: 100% !important;
        display: flex;
        flex-direction: column;
        padding-left: 0 !important;

        .content-header {
          padding: 4% 0 !important;

          h1 {
            font-family: "Noto Serif" !important;
            font-style: normal !important;
            font-weight: 300 !important;
            font-size: 24px !important;
            line-height: 30px !important;
          }
        }

        .img {
          padding-top: 3rem !important;
          width: 70% !important;
          height: 100% !important;
        }

        .content-para {
          p {
            font-family: "Outfit" !important;
            font-style: normal !important;
            font-weight: 300 !important;
            font-size: 16px !important;
            line-height: 20px !important;
            color: #9c9c9c !important;
          }
        }

        .content-button {
          margin: 0 !important;
          position: unset !important;
          justify-content: center;
          padding: 12% 0;

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
