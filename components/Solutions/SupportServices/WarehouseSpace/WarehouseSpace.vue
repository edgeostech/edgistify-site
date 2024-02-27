<template>
  <v-container fluid class="warehouse-space-main pa-0">
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-row no-gutters class="main_title" id="warehouse-space">
      <h1>Warehouse Space</h1>
    </v-row>
    <v-row no-gutters class="main_content">
      <v-col class="main_left_image" sm="12" md="6">
        <v-img
          src="/Solutions/supportservices/warehouse-spce-banner.png"
          contain
        />
      </v-col>
      <v-col class="main_right_content" sm="12" md="6">
        <div class="content-header pa-0">
          <h1>Affordable, Flexible and Secured Warehouses</h1>
        </div>
        <div class="content-para">
          <p>
            Get instant access to affordable and secured warehouses across
            India. We are equipped with state-of-the-art infrastructure and 24 x
            7 security surveillance. We manage over 4.5 Lac sq. ft. of space
            nationwide. Use our Pan-India warehouse network to store your
            products near your demand centers. Choose from multiple shared and
            dedicated warehouse options best suited for your business needs.
          </p>
        </div>
        <div class="content-button">
          <v-btn
            class="button bg-white"
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-anchor=".content-header"
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
      showModal: false,
      isSmalldevice: false,
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
@media (max-width: 850px) {
  .main_title {
    padding: 0 6% !important;
    h1 {
      font-size: 30px !important;
    }
  }

  .main_content {
    height: auto !important;

    .content-para {
      height: auto !important;
    }

    .content-header {
      height: auto !important;
      h1 {
        font-size: 24px !important;
        line-height: 30px !important;
      }
    }
    .main_left_image {
      padding-right: 0 !important;
    }

    .main_left_image,
    .main_right_content {
      width: 100vw !important;
      height: auto !important;
      margin: 0 !important;
    }

    .content-button {
      padding: 5% 20% !important;
      position: unset !important;
      display: flex;
      justify-content: center;
    }

    img {
      width: 88vw !important;
      height: 100%;
    }
  }
}

.warehouse-space-main {
  background: #f3f3f5;

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
      padding: 12px 12px 12px 0;
      color: white !important;
    }
  }

  .main_content {
    width: 100%;
    height: auto;
    display: flex;
    padding: 0 6%;

    .main_left_image {
      margin: 50px 0 50px 0 !important;
      padding-right: 58px;
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
          line-height: 40px;
          color: #000000;
        }
      }

      .content-para {
        width: 100%;
        margin-top: 1rem;
        padding-right: 2.5rem;

        p {
          font-family: "Outfit";
          font-style: normal;
          font-weight: 300;
          font-size: 16px;
          line-height: 20px;
          color: black;
        }
      }

      .content-para-list {
        width: 100%;
        margin-top: 1rem;
        border-left: 1px solid black;
        transform: rotate(0deg);

        .list {
          font-family: "Outfit";
          font-style: normal;
          font-weight: 300;
          font-size: 16px;
          line-height: 24px;
          margin-left: 1rem;
          color: black;
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
          font-family: "Noto Serif";
          text-transform: initial;
          font-style: normal;
          font-size: 18px;
          font-weight: 700;
          line-height: 25px;
          border: none;
          letter-spacing: 0px;

          // span {
          //    font-weight: 500 !important;
          // }

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
</style>
