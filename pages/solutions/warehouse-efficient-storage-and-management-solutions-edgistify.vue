<template>
  <v-container
    fluid
    class="solutions-warehouse-container pa-0"
    id="warehouse-container"
  >
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-row class="head-cover p-0" no-gutters>
      <v-col sm="6" md="6">
        <div class="left-head-cover">
          <div class="title">
            <div class="title_header">
              <p>Efficient Storage for Streamlined Operations</p>
            </div>
            <v-col class="dashboard_content">
              <p>
                Get the edge in logistics with our Best-in-Class Warehousing,
                Infrastructure and Fulfilment Service to fulfil your D2C, B2C,
                and B2B orders with seamless efficiency and reliability.
              </p>
            </v-col>
            <div class="title_button">
              <v-btn
                class="button bg-white"
                @click="showModal = true"
                data-aos="fade-up"
                data-aos-once="true"
                data-aos-easing="ease-in"
                data-aos-anchor=".title"
                data-aos-duration="1000"
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
              :src="`/Solutions/warehousing/warehouse-management-gif.gif`"
              alt=""
              aspect-ratio="1"
              cover
              class="bg-grey-lighten-2 image-gif"
            ></v-img>
          </div>
        </div>
      </v-col>
    </v-row>
    <ECommerceFulfillment />
    <DarkStoreOperations />
    <BToBRetailDistribution />
    <EdgistifyForm />
  </v-container>
</template>

<script>
import aosMixin from "~/mixins/aos";
import ECommerceFulfillment from "../../components/Solutions/Warehousing/ECommerceFulfillment/ECommerceFulfillment.vue";
import DarkStoreOperations from "../../components/Solutions/Warehousing/DarkStoreOperations/DarkStoreOperations.vue";
import BToBRetailDistribution from "../../components/Solutions/Warehousing/BToBRetailDistribution/BToBRetailDistribution.vue";
import EdgistifyForm from "../../components/EdgistifyForm/EdgistifyForm.vue";
import ConnectModal from "../../components/ModalForm/ConnectModal.vue";

export default {
  components: {
    ECommerceFulfillment,
    DarkStoreOperations,
    BToBRetailDistribution,
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
      title: "Warehouse Efficient Storage and Management Solutions Edgistify "
    };
  }
};
</script>

<style lang="scss" scoped>

.solutions-warehouse-container {
  display: flex;
  flex-direction: column;
  padding-top: 92px !important;
  // background-color: #0c0c0c;

  .head-cover {
    display: flex;
    align-items: center;
    justify-content: auto;
    background-color: #ffffff;

    .left-head-cover {
      .title {
        color: #1e1e1e;
        padding: 0 12%;

        .title_header {
          p {
            font-size: 46.61px;
            font-weight: 300;
            font-family: "Noto Serif";
            font-style: normal;
            line-height: 63px;
          }
        }

        .title_button {
          .button {
            display: flex;
            width: 11rem;
            height: 3rem;
            border: 1px solid #00a699;
            border-radius: 40px;
            color: #fff;
            padding: 0px 40px;
            font-family: "Noto Serif";
            text-transform: initial;
            font-style: normal;
            font-size: 18px;
            font-weight: 700;
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
      .head_image {
        display: flex;
        width: 100%;
        height: 100%;
        margin: 0 auto;
        overflow: hidden;

        .video-class {
          width: 100%;
          height: 100%;
          object-fit: fill;
        }
      }
    }
  }
}
@media (max-width: 850px) {

  .solutions-warehouse-container {
  padding-top: 0 !important;}
  .title_button {
    justify-content: center;
    display: flex;
  }
  .head-cover {
    flex-direction: column-reverse;
    padding: 0 !important;

    .left-head-cover {
      padding: 30px !important;
      .title {
        padding: 0 !important;
        .title_header {
          p {
            font-family: "Noto Serif" !important;
            font-style: normal !important;
            font-weight: 300 !important;
            font-size: 2rem !important;
            line-height: 2rem !important;
            color: #1e1e1e !important;
          }
        }
      }
    }

    .head_image {
      width: 100% !important;
      height: 100% !important;

      video {
        width: 100% !important;
      }
    }
  }
}


</style>
