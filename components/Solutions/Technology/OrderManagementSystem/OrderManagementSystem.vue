<template>
  <v-container fluid class="order-mngt-system-main pa-0">
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-row no-gutters class="main_content" id="oms">
      <v-col class="main_left_image" sm="12" md="6" v-if="!isSmallDevice">
        <img
          src="/Solutions/technology/order-management-system.jpg.png"
          contain
        />
      </v-col>
      <v-col class="main_right_content" sm="12" md="6">
        <v-col class="main_title">
          <h1>
            Order <br />
            Management System
          </h1>
        </v-col>
        <v-col class="content-header">
          <h1>Unified Order Processing with Real-time Data and Insights</h1>
        </v-col>
        <v-col class="main_left_image" v-if="isSmallDevice">
          <img
            src="/Solutions/technology/order-management-system.jpg.png"
            contain
            alt="Efficient order management system for streamlined operations"
          />
        </v-col>
        <v-col class="content-para">
          <p>
            Efficiently manage your orders from all channels on a unified
            dashboard. Our OMS allows you to streamline the process of
            receiving, processing and fulfilling orders by consolidating them on
            a single platform. One-click integrations with leading ERPs and
            accounting tools help you to synchronize stock, sales and purchasing
            information. As a result, you gain real-time visibility into your
            inventory levels, orders, and shipping information, which enables
            you to make informed decisions and quickly respond to changing
            customer demands.
          </p>
        </v-col>
        <v-col class="content-button">
          <v-btn
            class="button bg-white"
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="1000"
            @click="showModal = true"
            >Get in Touch</v-btn
          >
        </v-col>
      </v-col>
    </v-row>
    <v-row no-gutters class="stats">
      <v-col cols="12" sm="12" md="4" class="card">
        <h1>95.6%</h1>
        <p>Order Accuracy</p>
      </v-col>
      <v-col cols="12" sm="12" md="4" class="card">
        <h1>98%</h1>
        <p>Adherence to SLA</p>
      </v-col>
      <v-col cols="12" sm="12" md="4" class="card">
        <h1>49%</h1>
        <p>Reduction in Shipping Costs</p>
      </v-col>
    </v-row>
    <v-row class="main_point_detail" no-gutters>
      <v-col class="left_main" sm="12" md="6">
        <v-img
          :src="`/Solutions/technology/integration.png`"
          contain
          aspect-ratio="1"
        />
      </v-col>
      <v-col class="right_main mt-12 mb-12" sm="12" md="6">
        <ul class="right_main_container">
          <li class="right_main_title">
            <div class="right_main_top">
              <h1>Order Accuracy</h1>
              <img
                src="/Common/right-grp-dark.png"
                contain
                class="right-arrow"
              />
              <img src="/Common/down-grp-dark.png" contain class="down-arrow" />
            </div>
            <ul class="right_main_description">
              <p>
                Scan-based pick, pack and sort process, automating workflows.
              </p>
              <!-- <li>Fully-equipped facilities for e-commerce operations</li>
              <li>24x7 CCTV surveillance</li> -->
            </ul>
          </li>
          <li class="right_main_title">
            <div class="right_main_top">
              <h1>SLA Adherence</h1>
              <img
                src="/Common/right-grp-dark.png"
                contain
                class="right-arrow"
              />
              <img src="/Common/down-grp-dark.png" contain class="down-arrow" />
            </div>
            <ul class="right_main_description">
              <p>Doge SLA breach with timely order processing.</p>
            </ul>
          </li>
          <li class="right_main_title">
            <div class="right_main_top">
              <h1>Order Routing</h1>
              <img
                src="/Common/right-grp-dark.png"
                contain
                class="right-arrow"
              />
              <img src="/Common/down-grp-dark.png" contain class="down-arrow" />
            </div>
            <ul class="right_main_description">
              <p>
                Route orders to the nearest fulfillment center carrying the
                desired inventory, reducing ETA and shipping costs.
              </p>
            </ul>
          </li>
          <li class="right_main_title">
            <div class="right_main_top">
              <h1>Returns Management</h1>
              <img
                src="/Common/right-grp-dark.png"
                contain
                class="right-arrow"
              />
              <img src="/Common/down-grp-dark.png" contain class="down-arrow" />
            </div>
            <ul class="right_main_description">
              <p>
                Get highly automated hiccup-free returns ensuring tracking of
                items throughout the returns process.
              </p>
            </ul>
          </li>
          <li class="right_main_title">
            <div class="right_main_top">
              <h1>Omnichannel</h1>
              <img
                src="/Common/right-grp-dark.png"
                contain
                class="right-arrow"
              />
              <img src="/Common/down-grp-dark.png" contain class="down-arrow" />
            </div>
            <ul class="right_main_description">
              <p>
                Integrate marketplaces and web stores to manage your online
                orders on a single platform.
              </p>
            </ul>
          </li>
          <!-- <li class="right_main_title">
            <div class="right_main_top">
              <h1>Returns</h1>
              <img src="/Common/right-grp-dark.png" contain class="right-arrow" />
              <img src="/Common/down-grp-dark.png" contain class="down-arrow" />
            </div>
            <ul class="right_main_description">
              <li>Complete control over Non-deliveries and Returns</li>
              <li>Recirculate RTO and returns in the shortest time</li>
            </ul>
          </li> -->
        </ul>
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
.order-mngt-system-main {
  height: auto;
  background: #f3f3f5;

  .main_content {
    height: auto;

    .main_left_image {
      padding: 2% 3% 4% 6%;

      img {
        width: 100%;
        height: 100%;
      }
    }

    .main_right_content {
      padding: 0% 6% 0 3%;
      position: relative;

      .main_title {
        width: 100%;

        h1 {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 400;
          font-size: 42px;
          line-height: 57px;
          color: #0c0c0c;
        }
      }

      .content-header {
        width: 100%;
        padding-top: 2rem;

        h1 {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 300;
          font-size: 32px;
          line-height: 44px;
          color: #1e1e1e;
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
          color: #313131;
        }
      }

      .content-button {
        display: flex;
        position: absolute;
        bottom: 0;
        // margin: 40px 0 0 0;

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
          font-weight: 500;
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
              box-shadow: inset 178px 0 0 0 #000000;
              color: #ffffff;
            }
          }
        }
      }
    }
  }

  .stats {
    // width: 100%;
    height: 15.313rem;
    // display: flex;
    background: #00a699;

    .card {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      border-right: 1px solid whitesmoke;

      h1 {
        font-family: "Noto Serif";
        font-style: normal;
        font-weight: 600;
        font-size: 4rem;
        line-height: 87px;
        color: #ffffff;
      }

      p {
        font-family: "Outfit";
        font-style: normal;
        font-weight: 400;
        font-size: 1.125rem;
        line-height: 23px;
        color: #ffffff;
      }
    }
  }

  // .main_point_detail {
  //   height: auto;
  //   padding: 4% 6%;
  //   background-color: white;

  //   .left_main {
  //     width: 50%;
  //   }

  //   .right_main {
  //     .right_main_container {
  //       display: flex;
  //       height: auto;
  //       flex-direction: column;
  //       align-items: flex-start;

  //       .right_main_title {
  //         display: flex;
  //         align-items: center;
  //         justify-content: space-between;
  //         width: 100%;
  //         background: #ffffff;
  //         border-bottom: 1px solid rgba(12, 12, 12, 0.5);
  //         height: auto;

  //         h1 {
  //           font-family: "Outfit";
  //           font-style: normal;
  //           font-weight: 400;
  //           font-size: 26px;
  //           line-height: 40px;
  //           color: #1e1e1e;
  //         }

  //         &:hover {
  //           color: #ffffff;
  //         }
  //       }
  //     }
  //   }
  // }

  .main_point_detail {
    // background: #0c0c0c;
    background-color: white;

    .left_main {
      .v-image {
        height: 350px;
        margin: 6% 0;
      }
    }

    .right_main {
      .right_main_container {
        // background: #0c0c0c;
        background-color: white;

        padding: 0 6%;

        .right_main_title:hover .right_main_description {
          display: flex;
        }

        .right_main_title:hover .down-arrow {
          display: flex;
        }

        .down-arrow {
          display: none;
        }

        .right-arrow {
          display: block;
        }

        .right_main_title:hover .right-arrow {
          display: none;
        }

        .right_main_title:hover {
          border-bottom: 1px solid #00a699;
        }

        .right_main_title {
          display: flex;
          flex-direction: column;
          align-items: center;
          justify-content: space-between;
          width: 100%;
          // border-bottom: 1px solid rgba(255, 255, 255, 0.5);
          border-bottom: 1px solid rgba(12, 12, 12, 0.5);
          // margin: 6% 6% 6% 1%;
          padding: 3% 6% 2% 3%;
          cursor: pointer;

          // height: 50%;

          .right_main_top {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 100%;
            h1 {
              font-size: 26px !important;
              line-height: 40px !important;
            }
            p {
              font-size: 15px !important;
              line-height: 20px !important;
            }
          }

          .right_main_description {
            list-style-type: none;
            display: none;
            flex-direction: column;
            width: 100%;
            height: auto;
            padding: 0 !important;
            margin: 1em 0 1em 0;

            p {
              font-family: "Outfit";
              font-style: normal;
              font-weight: 400;
              font-size: 1em;
              line-height: 1.25rem;
              transition: all 0.3s ease-in-out;
              // color: #ffffff;
              color: #313131;
            }

            // li::before {
            //   content: "•";
            //   // color: white;
            //   color: #1E1E1E;
            //   display: inline-block;
            //   width: 1em;
            //   margin-left: 0em;
            // }
          }

          h1 {
            font-family: "Outfit";
            font-style: normal;
            font-weight: 400;
            font-size: 2rem;
            line-height: 40px;
            // margin: 0 0 5px 15px;

            // color: #ffffff;
            color: #1e1e1e;
          }

          &:hover {
            color: #ffffff;
          }
        }
      }
    }
  }
}

@media (max-width: 850px) {
  .order-mngt-system-main {
    .main_content {
      padding: 0% 6% !important;

      .main_right_content {
        padding: 0 !important;

        .main_title {
          h1 {
            color: #0c0c0c !important;
            font-weight: 500 !important;
            font-size: 30px !important;
            line-height: 2rem !important;
          }
        }

        .content-header {
          padding-top: 1rem !important;

          h1 {
            font-weight: 100 !important;
            font-size: 24px !important;
            line-height: 1.875rem !important;
          }
        }

        .main_left_image {
          padding: 4% 0 !important;

          img {
            padding-right: 10% !important;
          }
        }

        .content-para {
          p {
            font-size: 16px !important;
            line-height: 20px !important;
          }
        }

        .content-button {
          padding: 10% 25% !important;
          position: unset;
          justify-content: center;

          .button {
            display: flex;
            border: 1px solid #00a699;

            color: #ffffff;
            font-size: 14px !important;
            line-height: 20px !important;
            font-weight: 300 !important;

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

    .stats {
      height: 37.2rem !important;

      .card {
        border-bottom: 2px solid whitesmoke !important;
      }
    }

    .main_point_detail {
      width: 100% !important;
      height: auto !important;
      display: flex !important;
      flex-direction: column !important;

      .left_main {
        display: none;
      }

      .right_main {
        width: 100% !important;

        .right_main_container {
          display: flex;
          width: 100%;
          height: auto !important;
          flex-direction: column !important;
          align-items: flex-start !important;

          .right_main_title {
            h1 {
              font-size: 1.066rem !important;
              line-height: 1.313rem !important;
            }
          }
        }
      }
    }
  }
}
</style>
