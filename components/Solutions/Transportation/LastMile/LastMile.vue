<template>
  <v-container fluid class="last-mile-main pa-0">
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-row no-gutters id="first-mile">
      <div class="main_title">
        <h1>Last Mile</h1>
      </div>
    </v-row>
    <v-row class="main_content mt-0">
      <v-col class="main_left_content pa-0 pr-6" sm="12" md="6">
        <div class="content-header px-0">
          <h1>Deliver Lasting Impressions to Your Customer's Doorstep</h1>
        </div>
        <div class="content-para px-0">
          <p>
            Choose the most suitable courier partners to deliver your products
            more efficiently and effectively. Our partnerships with 18+ major
            courier partners and same-day fulfillment services across 30+ cities
            provide a robust courier and rider network that covers delivery
            across 18,000 pin codes in India. In addition, our reach across Tier
            1,2 and 3 helps you meet customer expectations in every corner of
            the country.
          </p>
        </div>
        <div class="content-para-list pa-0">
          <div class="list">Increased Efficiency</div>
          <div class="list">Competitive Advantage</div>
        </div>
        <div class="content-button px-0">
          <v-btn
            class="button bg-white"
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-anchor=".content-para"
            data-aos-duration="1000"
            @click="showModal = true"
            >Get in Touch</v-btn
          >
        </div>
      </v-col>
      <v-col class="main_right_image pb-12">
        <v-img
          :src="`/Solutions/transportation/last-mile-banner.png`"
          cover
          class="bg-grey-lighten-2 image-jpg"
        ></v-img>
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
      isSmallDevice: false,
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

.last-mile-main {
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
    height: auto;
    background: #ffffff;
    padding: 0 6%;

    .main_left_content {
      display: flex;
      flex-direction: column;
      margin: 50px 0 0 0;
      padding-left: 10px !important;
      position: relative;

      .content-header {
        width: 100%;

        h1 {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 300;
          font-size: 32px;
          line-height: 40px;
          color: black;
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

    .main_right_image {
      // width: 100%;
      height: auto;
      margin-top: 50px !important;
      // margin: 80px 0 0 0;
    }
  }
}
@media (max-width: 850px) {
  .last-mile-main {
    .main_title {
      h1 {
      font-size: 30px !important;
      }
    }
  }
  .main_content {
    height: auto !important;
    flex-direction: column-reverse !important;

    .main_left_content {
      margin-bottom: 20px !important;
      height: auto !important;
      margin-top: 0 !important;
    }

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

    .main_left_content,
    .main_right_image {
      height: auto !important;

      .content-button {
        padding: 5% 20% !important;
        position: unset !important;
        margin-bottom: 0 !important;
        display: flex;
        justify-content: center;
      }
    }

    img {
      width: 88vw !important;
      height: auto;
    }
  }
}

</style>
