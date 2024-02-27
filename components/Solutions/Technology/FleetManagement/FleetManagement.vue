<template>
  <v-container fluid class="fm-container pa-0">
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-row no-gutters class="main_content" id="fms">
      <v-col class="main_left_content">
        <v-col class="main_title px-0">
          <h1>Fleet Management</h1>
        </v-col>
        <v-col class="content-header px-0">
          <h1>
            Keep moving forward with our Fleet<br />
            Management System
          </h1>
        </v-col>
        <!-- Mobile Layout -->
        <v-col class="main_right_image px-0" v-if="isSmallDevice">
          <img src="/Solutions/technology/blank-fleet-banner.png" contain />
        </v-col>
        <!-- Mobile End -->
        <v-col class="content-para px-0 pr-md-12">
          <p>
            We help you strengthen your fleet capacity with end-to-end delivery
            management and optimization. Our fleet management system provides
            real-time fleet visibility to oversee all fleet performance and
            fleet maintenance, increasing productivity and decreasing access
            usage of fuel with predictive analytics and accurate reporting.<br />
            <br />
            Automate Delivery Scheduling with real-time tracking alerts and
            updates. With advanced geocoding capabilities and AI-enabled route
            planning, we help you plan your deliveries with great accuracy and
            meet all your delivery SLAs<br />
          </p>
        </v-col>
        <v-col class="content-button px-0">
          <v-btn class="button primaryColor" @click="showModal = true"
            >Get in Touch</v-btn
          >
        </v-col>
      </v-col>
      <v-col class="main_right_image" v-if="!isSmallDevice">
        <img src="/Solutions/technology/blank-fleet-banner.png" contain />
      </v-col>
    </v-row>
    <v-row no-gutters class="other-content">
      <v-col class="other-left">
        <v-col class="other-content-header px-0">
          <h1>
            Increase fleet efficiency and reduce<br />
            operational costs
          </h1>
        </v-col>
        <v-col class="other-left-image px-0" v-if="!isSmallDevice">
          <img src="/Solutions/technology/truck-web.png" contain />
        </v-col>
        <v-col class="other-left-image px-0" v-if="isSmallDevice">
          <img src="/Solutions/technology/truck-mob.png" contain />
        </v-col>
      </v-col>
      <v-col class="other-right">
        <v-col class="right-list px-0">
          <v-col class="right_main_title">
            <p>Real-time tracking of vehicles</p>
          </v-col>
          <v-col class="right_main_title">
            <p>Seamless monitoring of fuel consumption and mileage</p>
          </v-col>
          <v-col class="right_main_title">
            <p>Real-time delay prediction</p>
          </v-col>
          <v-col class="right_main_title">
            <p>Duration at Loading/Unloading points</p>
          </v-col>
          <v-col class="right_main_title">
            <p>
              Geofence alerts for vehicles entering/exiting from a particular
              location
            </p>
          </v-col>
          <v-col class="right_main_title">
            <p>Reduce accidents and breakdowns</p>
          </v-col>
          <v-col class="right_main_title">
            <p>
              Precise location on the map with various vehicle health data e.g:
              speed, rpm, fuel <br />
              consumption, km, coolant temperature, etc
            </p>
          </v-col>
          <v-col class="right_main_title">
            <p>Intelligent Route planning</p>
          </v-col>
          <v-col class="right_main_title">
            <p>
              Check Tolls on the route in the map with tax information, Save
              expenses, RTO, and <br />
              other tax information with routes
            </p>
          </v-col>
          <v-col class="right_main_title">
            <p>
              Automatic tracking of the assigned route with the actual route
              taken by the driver
            </p>
          </v-col>
        </v-col>
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
.fm-container {
  height: auto;
  background: #f3f3f5;

  .main_content {
    height: auto;
    padding: 0 6%;

    .main_left_content {
      height: auto;

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
        height: auto;

        p {
          width: 100%;
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
        padding: 15% 0 0 0;

        .button {
          display: flex;
          height: 40px;
          width: 170px;
          border-radius: 73px;
          text-transform: capitalize;
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
              box-shadow: inset 178px 0 0 0 #000000;
              color: #ffffff;
            }
          }
        }
      }
    }

    .main_right_image {
      height: auto;
      flex-direction: column;

      img {
        width: 100%;
      }
    }
  }

  .other-content {
    height: auto;
    background-color: #ffffff;
    padding: 4% 6%;

    .other-left {
      height: auto;

      .other-content-header {
        height: auto;

        h1 {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 300;
          font-size: 32px;
          line-height: 44px;
          color: #1e1e1e;
        }
      }

      .other-left-image {
        height: auto;

        img {
          height: auto;
        }
      }
    }

    .other-right {
      height: auto;

      .right-list {
        height: auto;

        .right_main_title {
          border-bottom: 1px solid rgba(49, 49, 49, 0.5);

          p {
            font-family: "Outfit";
            font-style: normal;
            font-weight: 300;
            font-size: 16px;
            line-height: 20px;
            color: #313131;
          }
        }
      }
    }
  }
}

@media (max-width: 850px) {
  .fm-container {
    .main_content {
      height: auto !important;

      .main_left_content {
        height: auto !important;

        .main_title {
          h1 {
            font-size: 30px !important;
          }
        }

        .content-header {
          h1 {
            font-weight: 100 !important;
            font-size: 24px !important;
          }
        }

        .main_right_image {
          height: auto !important;

          img {
            width: 100% !important;
            height: auto !important;
          }
        }

        .content-para {
          p {
            font-size: 0.75rem !important;
            line-height: 0.938rem !important;
          }
        }

        .content-button {
          display: flex !important;
          padding: 5% 20% !important;

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

    .other-content {
      flex-direction: column !important;

      .other-left {
        height: auto !important;

        .other-content-header {
          height: auto;

          h1 {
            font-size: 1.5rem !important;
            line-height: 2rem !important;
          }
        }

        .other-left-image {
          height: auto;

          img {
            width: 100% !important;
            height: auto !important;
          }
        }
      }

      .other-right {
        height: auto !important;

        .right-list {
          .right_main_title {
            p {
              font-size: 0.75rem !important;
              line-height: 0.938rem !important;
            }
          }
        }
      }
    }
  }
}
</style>
