<template>
  <v-container fluid class="wms-container pa-0">
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-row no-gutters class="main_content" id="wms">
      <v-col class="main_left_content" sm="12" md="6">
        <v-col class="main_title px-0">
          <h1>
            Warehouse <br />
            Management System
          </h1>
        </v-col>
        <v-col class="content-header px-0">
          <h1>
            Increased Efficiency and Control Across Warehouses
          </h1>
        </v-col>
        <!-- Mobile Layout -->
        <v-col class="main_right_image px-0" v-if="isSmallDevice">
          <img src="/Solutions/technology/warehouse-management-system-software.png" contain />
        </v-col>
        <!-- Mobile End -->
        <v-col class="content-para px-0">
          <p>
            Manage multiple warehouses in different locations, track and transfer products across warehouses based on
            demand, streamline operations and generate insightful reports.

            Our WMS ensures that all resources are put to optimum utilization. In addition, it helps to automate warehouse
            processes to monitor the inbound and outbound movement of goods and maintain accurate stock levels at all times.
          </p>
        </v-col>
        <v-col class="content-button px-0">
          <v-btn class="button bg-black" @click="showModal = true">Schedule a Call</v-btn>
        </v-col>
      </v-col>
      <v-col class="main_right_image" sm="12" md="6" v-if="!isSmallDevice">
        <v-img src="/Solutions/technology/warehouse-management-system-software.png" contain />
      </v-col>
    </v-row>
    <v-row no-gutters class="wms-perks">
      <v-row no-gutters class="cards-container">
        <v-col cols="12" sm="12" md="4" class="pr-md-6 pb-6 pr-sm-0">
          <div class="card">
            <div class="icon-container multi-loc-warehouse"></div>
            <div class="title">
              Multi-Location <br />
              Warehouse Management
            </div>
            <div class="paragraph">
              Get central control of all your warehouses. Manage stock at multiple locations and effortlessly keep track of
              stock transfers within your warehouses.
            </div>
          </div>
        </v-col>
        <v-col cols="12" sm="12" md="4" class="px-md-6 pb-6 pl-sm-0">
          <div class="card">

            <div class="icon-container real-time-stock-updates"></div>
            <div class="title">
              Real-Time Stock <br />
              Level Updates
            </div>
            <div class="paragraph">
              Manage your stock on the go. Monitor stock levels whenever you create a sale or purchase order and keep
              complete track of your inventory.
            </div>
          </div>
        </v-col>
        <v-col cols="12" sm="12" md="4" class="pl-md-6 pb-6 pl-sm-0">
          <div class="card">

            <div class="icon-container reports-insights"></div>
            <div class="title">
              Reports <br />
              and Insights
            </div>
            <div class="paragraph">
              Create customized reports to monitor your orders status, SLA and inventory. Get actionable insights and adapt to
              changing customer needs.
            </div>
          </div>
        </v-col>
      </v-row>
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
      isSmallDevice: false,
      showModal: false,
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

<style lang="scss" scoped>
.wms-container {
  height: auto;

  .main_content {
    height: auto;
    padding: 4% 6%;

    .main_left_content {
      height: auto;
      padding: 0 6% 0 0;
      position: relative;

      .main_title {
        width: 100%;

        h1 {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 400;
          font-size: 42px;
          line-height: 57px;
          text-align: center;
          color: #ffffff;
          text-align: left;
        }
      }

      .content-header {
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
        position: absolute;
        bottom: 0;

        .button {
          display: flex;
          height: 48px;
          width: 178px;
          border-radius: 73px;
          text-transform: inherit;
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 400;
          font-size: 18px;
          line-height: 25px;
          color: #ffffff;
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
              box-shadow: inset 178px 0 0 0 #ffffff;
              color: #000000;
            }
          }
        }
      }
    }

    .main_right_image {
      height: auto;

      img {
        width: 19.063rem;
        height: 25.438rem;
      }
    }
  }

  .wms-perks {
    height: 100%;
    background: #fdfdfd;

    .cards-container {
      height: 100%;
      padding: 4% 6%;

      .card {
        display: flex;
        height: 20rem;
        flex-direction: column;
        align-items: flex-start;
        justify-content: center;
        background-color: #f3f3f5;

        .icon-container {
          display: flex;
          align-items: center;
          justify-content: center;
          width: 100%;
          height: 20%;
          background-size: auto;
          background-position-x: left;
          margin-left: 5%;
          // margin-left: 3rem;

          &.multi-loc-warehouse {
            background-image: url("/Solutions/technology/multi-loc-warehouse.png");
          }

          &.real-time-stock-updates {
            background-image: url("/Solutions/technology/real-time-stock-updates.png");
          }

          &.inventory-management {
            background-image: url("/Solutions/technology/inventory-management.png");
          }

          &.reports-insights {
            background-image: url("/Solutions/technology/reports-insights.png");
          }
        }

        .title {
          display: flex;
          text-align: left;
          align-items: center;
          justify-content: left;
          width: 100%;
          height: 30%;
          font-weight: 500;
          font-size: 1rem;
          color: #000000;
          margin-left: 5%;
          font-family: 'Noto Serif' !important;
        }

        .paragraph {
          width: 80%;
          font-family: "Outfit";
          font-style: normal;
          font-weight: 300;
          font-size: 1rem;
          line-height: 20px;
          color: #313131;
          margin-left: 5%;
        }
      }
    }
  }
}

@media (max-width: 850px) {
  .wms-container {
    .main_content {
      height: auto !important;

      .main_left_content {
        height: auto !important;
        // flex-direction: column !important;
        padding: 0 !important;

        .main_title {
          h1 {
            font-weight: 500 !important;
            font-size: 30px !important;
            line-height: 2rem !important;
          }
        }

        .content-header {
          h1 {
            font-weight: 100 !important;
            font-size: 24px !important;
            line-height: 1.875rem !important;
          }
        }

        .main_right_image {
          img {
            width: 100% !important;
            height: 100% !important;
          }
        }

        .content-para {
          p {
            font-size: 16px !important;
            line-height: 20px !important;
          }
        }

        .content-button {
          padding: 10% 20% !important;
          justify-content: center;
          position: unset;

          .button {
            height: 2.5rem !important;
            width: 12rem !important;
            font-size: 14px !important;
      line-height: 20px !important;
      font-weight: 300 !important;
            span {
              font-weight: 300 !important;
            }
          }
        }
      }
    }

    .wms-perks {
      // width: 100% !important;
      // flex-direction: column !important;
      // padding-bottom: 10% !important;

      .cards-container {
        // flex-direction: column !important;
        // align-items: baseline !important;
        // padding: 5% 5% 0% 15% !important;
        // height: auto !important;

        .card {
          // width: 100% !important;
          height: 16rem !important;

          .icon-container {
            background-size: 12% !important;

            &.multi-loc-warehouse {
              background-image: url("/Solutions/technology/multi-loc-warehouse.png");
            }

            &.real-time-stock-updates {
              background-image: url("/Solutions/technology/real-time-stock-updates.png");
            }

            &.inventory-management {
              background-image: url("/Solutions/technology/inventory-management.png");
            }

            &.reports-insights {
              background-image: url("/Solutions/technology/reports-insights.png");
              background-size: 9% !important;
            }
          }

          .title {
            font-size: 20px !important;
            line-height: 24px !important;
          }

          .paragraph {
            font-size: 10px !important;
            line-height: 14px !important;
          }
        }
      }
    }
  }
}
</style>
