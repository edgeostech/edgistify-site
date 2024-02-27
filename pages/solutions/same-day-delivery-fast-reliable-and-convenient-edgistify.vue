<template>
  <v-container
    fluid
    class="solutions-sameday-container pa-0"
    id="solutions-sameday-container"
  >
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-row class="head-cover p-0" no-gutters>
      <v-col sm="12" md="6">
        <div class="left-head-cover">
          <div class="title">
            <div class="title_header">
              <p>Same Day Delivery to Exceed Customer Expectations</p>
            </div>
            <v-col class="dashboard_content">
              <p>
                Get ahead of the competition with our Same Day Delivery service.
                Exceed your customers' expectations and ensure fast and reliable
                delivery of your products.
              </p>
            </v-col>
            <div class="title_button">
              <v-btn class="button bg-white" @click="showModal = true"
                >Get in Touch</v-btn
              >
            </div>
          </div>
        </div>
      </v-col>
      <v-col sm="12" md="6">
        <div class="right-head-cover">
          <div class="head_image">
            <v-img
              :src="`/Solutions/warehousing/same-day-delivery-management.gif.gif`"
              alt="Same day delivery management process"
              aspect-ratio="1"
              cover
              class="bg-grey-lighten-2 image-gif"
            ></v-img>
          </div>
        </div>
      </v-col>
    </v-row>

    <Features />
    <DirectToConsumer />
    <EnterpriseBrands />
    <Ecommerce />
    <BenefitsOfSameDay />
    <EdgistifyForm />
  </v-container>
</template>

<script>
import aosMixin from "~/mixins/aos";
import Features from "../../components/Solutions/SameDayDelivery/Features/Features.vue";
import DirectToConsumer from "../../components/Solutions/SameDayDelivery/DirectToConsumer/DirectToConsumer.vue";
import EnterpriseBrands from "../../components/Solutions/SameDayDelivery/EnterpriseBrands/EnterpriseBrands.vue";
import Ecommerce from "../../components/Solutions/SameDayDelivery/ECommerce/ECommerce.vue";
import BenefitsOfSameDay from "../../components/Solutions/SameDayDelivery/BenefitsOfSameDay/BenefitsOfSameDay.vue";
import EdgistifyForm from "../../components/EdgistifyForm/EdgistifyForm.vue";
import ConnectModal from "../../components/ModalForm/ConnectModal.vue";

export default {
  components: {
    Features,
    DirectToConsumer,
    EnterpriseBrands,
    Ecommerce,
    BenefitsOfSameDay,
    EdgistifyForm,
    ConnectModal,
  },
  mixins: [aosMixin],
  data() {
    return {
      showModal: false,
    };
  },
  head() {
    return {
      title: "Same Day Delivery Fast Reliable and Convenient Edgistify ",
    };
  },
};
</script>

<style lang="scss" scoped>
.solutions-sameday-container {
  display: flex;
  flex-direction: column;
  width: 100%;
  height: auto;
  padding-top: 92px !important;
  // background-color: #0c0c0c;
  // padding-top: 100px;

  .head-cover {
    display: flex;
    width: 100%;
    height: 555px;
    align-items: center;
    justify-content: auto;
    background-color: #ffffff;
    padding: 0 0 0 6%;

    .left-head-cover {
      .title {
        display: flex;
        width: 100%;
        height: 100%;
        flex-direction: column;
        justify-content: center;
        color: #1e1e1e;

        .title_header {
          p {
            font-family: "Noto Serif";
            font-style: normal;
            font-weight: 300;
            font-size: 46.61px;
            line-height: 60px;
            color: #1e1e1e;
          }
        }

        .title_button {
          display: flex;

          .button {
            display: flex;
            height: 48px;
            width: 178px;
            border: 1px solid #00a699;
            border-radius: 40px;
            color: #fff;
            padding: 0px 40px;
            font-family: "Noto Serif";
            text-transform: initial;
            font-size: 18px;
            font-weight: 800;
            border: none;
            letter-spacing: 0px;

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

    .right-head-cover {
      display: flex;
      width: 100%;
      height: 555px;

      .head_image {
        display: flex;
        width: 100%;
        height: 100%;
        margin: 0 auto;
        overflow: hidden;

        video {
          width: 100%;
          height: 100%;
          object-fit: fill;
        }
      }
    }
  }
}
@media (max-width: 850px) {
  .solutions-sameday-container {
    height: auto !important;
    background-color: #0c0c0c;
    padding-top: 0 !important;

    .head-cover {
      flex-direction: column-reverse !important;
      height: auto !important;
      padding: 0 !important;

      .left-head-cover {
        width: 100% !important;
        height: auto !important;
        padding: 0 6% !important;

        .title {
          flex-direction: column !important;
          justify-content: center !important;
          color: #1e1e1e !important;

          .title_header {
            display: flex !important;
            padding: 50px 0 0 0 !important;
            width: 100% !important;
            height: auto !important;

            p {
              font-family: "Noto Serif" !important;
              font-style: normal !important;
              font-weight: 300 !important;
              font-size: 2rem !important;
              line-height: 2rem !important;
              color: #1e1e1e !important;
            }
          }

          .title_button {
            justify-content: center !important;
            padding-bottom: 6%;

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

      .right-head-cover {
        display: flex;
        width: 100% !important;
        height: auto !important;

        .head_image {
          display: flex;
          width: 100%;
          height: 100%;
          margin: 0 auto;
          overflow: hidden;

          video {
            width: 100%;
            height: 100%;
            object-fit: cover;
          }
        }
      }
    }
  }
}
</style>
