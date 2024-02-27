<template>
  <v-container fluid class="edge-os-container pa-0">
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-row no-gutters class="main_content">
      <v-col class="main_left_content" md="6" sm="12">
        <v-col class="main_title px-0">
          <h1>EdgeOS</h1>
        </v-col>
        <v-col class="content-header px-0">
          <h1>Unified Tech Platform for End-to-End Fulfillment</h1>
        </v-col>
        <v-col class="content-para px-0">
          <p>
            EdgeOS is a comprehensive portal that enables you to gain end-to-end
            visibility of your supply chain processes. It provides real-time
            data access, empowering you to control your inventory, order
            processing, and delivery processes. In addition, EdgeOS facilitates
            seamless connectivity across multiple warehouses and all
            stakeholders in the supply chain, enabling agile decision-making to
            adapt quickly to changing demand and delivery constraints.
          </p>
        </v-col>

        <v-col class="content-button">
          <v-btn class="button bg-black" @click="showModal = true"
            >Get in Touch</v-btn
          >
        </v-col>
      </v-col>
      <v-col class="main_right_image" md="6" sm="12">
        <!-- <img src="/Solutions/technology/edgeos-banner.png" contain /> -->
        <v-img
          src="/Solutions/technology/oms-wms-edgeos.jpg.png"
          contain
          alt="Enhance your business operations with EdgeOS order and warehouse management solution"
        />
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
      isSmallDevice: false,
      showModal: false,
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
.edge-os-container {
  height: auto;

  .main_content {
    height: auto;

    .main_left_content {
      height: auto;
      padding: 6% 6%;

      .main_title {
        width: 100%;
        display: flex;
        align-items: baseline;

        h1 {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 500;
          font-size: 42px;
          line-height: 57px;
          text-align: center;
          color: #ffffff;
        }
      }

      .content-header {
        width: 100%;
        padding-top: 2rem;

        h1 {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 100;
          font-size: 32px;
          line-height: 44px;
          color: #ffffff;
        }
      }

      .content-para {
        width: 100%;
        padding-top: 2.5rem;

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
        margin: 10% 0 0 0;

        .button {
          display: flex;
          border: 1px solid #00a699;
          border-radius: 73px;
          text-transform: initial;
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 400;
          font-size: 18px;
          line-height: 25px;
          color: #ffffff;
          //border:none;
          letter-spacing: 0px;

          span {
            font-weight: 500 !important;
          }

          &.primary {
            background-color: #00a699;
            box-shadow: inset 0 0 0 0 #00a699;
            transition: color 0.3s ease-in-out, box-shadow 0.3s ease-in-out;

            &:hover {
              box-shadow: inset 178px 0 0 0 #ffffff;
              color: #000000;
            }
          }
        }
      }
    }

    .main_right_image {
      background: #f3f3f5;
      padding: 6% 6%;

      img {
        width: 100%;
        height: 100%;
      }
    }
  }
}

@media (max-width: 850px) {
  .edge-os-container {
    height: auto !important;
    flex-direction: column-reverse !important;

    .main_content {
      .main_left_content {
        height: auto !important;
        padding: 0 !important;

        .main_title {
          padding: 6% 6% !important;

          h1 {
            font-weight: 400 !important;
            font-size: 30px !important;
            line-height: 2.063rem !important;
            text-align: center !important;
          }
        }

        .content-header {
          padding: 0 6% !important;

          h1 {
            font-weight: 300 !important;
            font-size: 24px !important;
            line-height: 1.875rem !important;
            color: #ffffff;
          }
        }

        .main_right_image {
          // background: #0c0c0c !important;
          padding: 6% 6% !important;
        }

        .content-para {
          padding: 6% 6% !important;

          p {
            font-weight: 300;
            font-size: 16px !important;
            line-height: 20px !important;
            color: #9c9c9c;
          }
        }

        .content-button {
          margin: 0 !important;
          padding: 6% 20% !important;
          justify-content: center !important;

          .button {
            display: flex;
            border: 1px solid #00a699;
            color: #ffffff;
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
            }
          }
        }
      }
    }
  }
}
</style>
