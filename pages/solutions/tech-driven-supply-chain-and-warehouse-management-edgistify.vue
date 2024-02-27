<template>
  <v-container
    fluid
    class="solutions-technology-container pa-0"
    id="solutions-technology-container"
  >
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-row no-gutters class="head-cover">
      <v-col class="left-head-cover" md="6" sm="12">
        <div class="title">
          <v-col class="title_header pa-0">
            <p>Streamline Your Supply Chain with Comprehensive Technology</p>
          </v-col>
          <v-col class="dashboard_content">
            <p>
              Future-proof your business with technology solutions suitable for
              your supply chain. We help you simplify every stage of your supply
              chain and gain complete visibility of orders and inventory on a
              single dashboard.
            </p>
          </v-col>
          <v-col class="title_button">
            <v-btn
              class="button bg-white"
              data-aos="fade-up"
              data-aos-once=" true"
              data-aos-easing="ease-in"
              data-aos-anchor=".title"
              data-aos-duration="1000"
              @click="showModal = true"
              >Get in Touch</v-btn
            >
          </v-col>
        </div>
      </v-col>
      <v-col class="right-head-cover pa-0" md="6" sm="12">
        <v-col class="head_image pa-0">
          <v-img
            :src="`/Solutions/warehousing/edgistify-advance-technology-solutions.gif.gif`"
            alt="Advanced technology solutions for optimized supply chain management"
            aspect-ratio="1"
            cover
            class="bg-grey-lighten-2"
          ></v-img>
        </v-col>
      </v-col>
    </v-row>
    <EdgeOS />
    <TechBenefits />
    <OrderManagementSystem />
    <WarehouseManagementSystem />
    <TechIntegrations />
    <PlatformOffers />
    <EdgistifyForm />
    <!-- <FleetManagement /> -->
  </v-container>
</template>

<script>
import aosMixin from "~/mixins/aos";
import EdgeOS from "../../components/Solutions/Technology/EdgeOS/EdgeOS.vue";
import TechBenefits from "../../components/Solutions/Technology/TechBenefits/TechBenefits.vue";
import OrderManagementSystem from "../../components/Solutions/Technology/OrderManagementSystem/OrderManagementSystem.vue";
import WarehouseManagementSystem from "../../components/Solutions/Technology/WarehouseManagementSystem/WarehouseManagementSystem.vue";
import TechIntegrations from "../../components/Solutions/Technology/TechIntegrations/TechIntegrations.vue";
//import EdgistifyFormTech from "../../components/Solutions/Technology/EdgistifyFormTech/EdgistifyFormTech.vue";
import EdgistifyForm from "../../components/EdgistifyForm/EdgistifyForm.vue";
import PlatformOffers from "../../components/Solutions/Technology/PlatformOffers/PlatformOffers.vue";
// import FleetManagement from "../../components/Solutions/Technology/FleetManagement/FleetManagement.vue";
import ConnectModal from "../../components/ModalForm/ConnectModal.vue";

export default {
  components: {
    EdgeOS,
    TechBenefits,
    OrderManagementSystem,
    WarehouseManagementSystem,
    TechIntegrations,
    EdgistifyForm,
    PlatformOffers,
    // FleetManagement,
    ConnectModal,
  },
  mixins: [aosMixin],
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
  head() {
    return {
      title: "Tech Driven Supply Chain and Warehouse Management Edgistify ",
    };
  },
};
</script>

<style lang="scss" scoped>
.solutions-technology-container {
  height: auto;
  background-color: #0c0c0c;
  padding-top: 92px !important;

  .head-cover {
    height: auto;

    .left-head-cover {
      height: auto;
      background-color: #ffffff;
      padding: 0 6%;
      padding-top: 6%;
      .title {
        display: flex;
        // width: 100%;
        height: 100%;
        flex-direction: column;
        justify-content: center;
        color: #1e1e1e;

        .title_header {
          display: flex;
          width: 100%;
          height: 302px;

          p {
            font-family: "Noto Serif";
            font-style: normal;
            font-weight: 100;
            font-size: 46.61px;
            line-height: 60px;
            color: #1e1e1e;
          }
        }

        .dashboard_content {
          width: 100%;

          p {
            font-family: "Outfit";
            font-style: normal;
            font-weight: 300;
            font-size: 16px;
            line-height: 20px;
            color: #0c0c0c;
          }
        }

        .title_button {
          display: flex;
          padding-left: 0;

          .button {
            display: flex;
            border: 1px solid #00a699;
            border-radius: 40px;
            color: #fff;
            padding: 0px 40px;
            font-family: "Noto Serif";
            text-transform: capitalize;
            font-size: 18px;
            font-style: normal;
            font-weight: 500;
            font-size: 18px;
            line-height: 25px;
            // border:none;
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
      height: auto;

      .head_image {
        height: auto;
        margin: 0 auto;
        overflow: hidden;
        background: #0c0c0c;

        video {
          width: 100%;
          height: 100%;
          object-fit: cover;
        }
      }
    }
  }

  // .dashboard-main {
  //   display: flex;
  //   background: #f3f3f5;
  //   border: 1px solid #f3f3f5;
  //   height: auto;
  //   width: 100%;

  //   .main-left {
  //     // width: 50%;
  //     // margin: 25px 0 25px 100px;
  //     padding: 6% 6%;

  //     .mac_image {
  //       img {
  //         width: 100%;
  //         height: 100%;
  //       }
  //     }
  //   }

  //   .main-right {
  //     // width: 50%;
  //     // margin: 80px 0 0 0;
  //     padding: 6% 0;

  //     .dashboard_content {
  //       width: 100%;

  //       p {
  //         font-family: "Outfit";
  //         font-style: normal;
  //         font-weight: 300;
  //         font-size: 16px;
  //         line-height: 20px;
  //         color: #0c0c0c;
  //       }
  //     }

  //     .dashboard_button {
  //       display: flex;
  //       padding: 15% 0;

  //       .button {
  //         display: flex;
  //         height: 42px;
  //         width: 172px;
  //         border: 1px solid #00a699;
  //         border-radius: 40px;
  //         color: #fff;
  //         padding: 0px 40px;
  //         font-family: "Noto Serif";
  //         text-transform: initial;
  //         font-size: 18px;
  //         font-style: normal;
  //         font-weight: 500;
  //         font-size: 18px;
  //         line-height: 25px;
  //         border: none;
  //         letter-spacing: 0px;

  //         span {
  //           font-weight: 500 !important;
  //         }

  //         &.primary {
  //           background-color: #00a699;
  //           box-shadow: inset 0 0 0 0 #00a699;
  //           transition: color 0.3s ease-in-out, box-shadow 0.3s ease-in-out;

  //           &:hover {
  //             box-shadow: inset 178px 0 0 0 #000000;
  //             color: #ffffff;
  //           }
  //         }
  //       }
  //     }
  //   }
  // }
}

@media (max-width: 850px) {
  .solutions-technology-container {
    display: flex !important;
    flex-direction: column !important;
    width: 100% !important;
    height: auto !important;
    background-color: #0c0c0c !important;
    overflow-x: clip !important;
    padding-top: 0 !important;

    .head-cover {
      flex-direction: column-reverse !important;
      height: auto !important;

      .right-head-cover {
        display: flex !important;
        width: 100% !important;
        height: 355px !important;

        .head_image {
          video {
            max-width: 100% !important;
          }
        }
      }

      .left-head-cover {
        height: auto !important;
        background-color: #ffffff !important;
        padding: 6% 6% !important;

        .title {
          height: auto !important;
          color: #1e1e1e !important;

          .title_header {
            height: 215px !important;

            p {
              font-family: "Noto Serif" !important;
              font-style: normal !important;
              font-weight: 300 !important;
              color: #1e1e1e !important;
            }
          }

          .title_button {
            display: flex !important;
            padding: 0 20% 10% 20% !important;
            justify-content: center;

            .button {
              span {
                font-weight: 500 !important;
              }

              &.primary {
                background-color: #00a699 !important;
                box-shadow: inset 0 0 0 0 #00a699 !important;
                transition: color 0.3s ease-in-out, box-shadow 0.3s ease-in-out !important;
              }
            }
          }
        }
      }
    }

    .dashboard-main {
      display: flex;
      background: #f3f3f5;
      // border: 1px solid #e7e7e7 !important;
      flex-direction: column !important;
      height: auto;
      // width: 100% !important;

      .main-left {
        padding: 0 6% !important;

        .mac_image {
          img {
            width: 100% !important;
            height: 100% !important;
          }
        }
      }

      .main-right {
        width: 100% !important;
        margin: 10% 0 0 0 !important;
        padding: 0 6% !important;

        .dashboard_content {
          width: 100%;
          display: flex !important;
          align-items: center !important;
          justify-content: center !important;

          p {
            font-size: 0.8rem !important;
          }
        }

        .dashboard_button {
          width: 100% !important;
          display: flex;
          padding: 10% 0 10% 0 !important;
          justify-content: center !important;

          .button {
            height: 2.473rem !important;
            width: 9.169rem !important;
            font-size: 14px !important;
            line-height: 20px !important;
            font-weight: 300 !important;
            span {
              font-weight: 300 !important;
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
