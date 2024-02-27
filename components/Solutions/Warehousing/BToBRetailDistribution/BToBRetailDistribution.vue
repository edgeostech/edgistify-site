<template>
  <v-container fluid class="b2b-retail-main">
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-row id="b2b_retail">
      <div class="main_title">
        <h1>B2B Logistics</h1>
      </div>
    </v-row>
    <v-row class="main_content">
      <v-col md="6" sm="12" class="main_left_content pa-0">
        <!-- <img src="/Solutions/warehousing/ds-banner.png" contain> -->
        <div class="content-header">
          <h1>Tailor-made B2B Distribution</h1>
        </div>
        <div class="content-para">
          <p>
            Implement the distribution strategy most suitable for your business.
            Hassle-free movement of goods from your suppliers to distributors
            and distributors to retailers.
          </p>
        </div>
        <div class="content-para-list">
          <div class="list">Reduced Pickup and Delivery Costs</div>
          <div class="list">Flexible Pickups</div>
          <div class="list">Precise Manifestation</div>
        </div>
        <div class="content-button mb-12">
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
      <v-col md="6" sm="12" class="main_right_image pa-0 pb-12">
        <v-img
          src="/Solutions/warehousing/optimized-b2b-logistics-solutions.jpg.jpg"
          alt="Optimized B2B logistics solutions for efficient supply chain management"
          contain
          style="margin-top: 50px"
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
      showModal: false,
    };
  },
};
</script>

<style lang="scss" scoped>
@media (max-width: 850px) {
  .main_title { 
    h1 {
      font-size: 30px !important
    }
  }
  .content-header {
    h1 {
      font-size: 24px !important;
    }
  }
  .main_content {
    flex-wrap: wrap;
    height: auto !important;
    flex-direction: column-reverse;

    .content-para {
      height: auto !important;
    }

    .content-header {
      height: auto !important;
    }

    .main_left_content {
      margin: 0 !important;
    }

    .main_left_content .content-button {
      justify-content: center;
      position: unset !important;
    }
  }
}

.b2b-retail-main {
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
      color: #ffffff;
      padding: 12px;
    }
  }

  .main_content {
    justify-content: space-between;
    background: #ffffff;
    padding: 0 6% !important;

    .main_left_content {
      flex-direction: column;
      margin: 50px 0 0 0;
      position: relative;

      .content-header {
        h1 {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 300;
          font-size: 32px;
          line-height: 44px;
          color: #0c0c0c;
        }
      }

      .content-para {
        // height: 260px;
        margin-top: 1rem;

        p {
          font-family: "Outfit";
          font-style: normal;
          font-weight: 300;
          font-size: 16px;
          line-height: 20px;
          color: #313131;
        }
      }

      .content-para-list {
        margin-top: 2rem;
        border-left: 1px solid #313131;
        transform: rotate(0deg);

        .list {
          font-family: "Outfit";
          font-style: normal;
          font-weight: 400;
          font-size: 16px;
          line-height: 28px;
          margin-left: 1rem;
          color: #313131;
        }
      }

      .content-button {
        display: flex;
        margin: 40px 0 0 0;
        position: absolute;
        bottom: 0;

        .button {
          display: flex;
          width: 11rem;
          height: 3rem;
          // border: 1px solid #00a699;
          border-radius: 73px;
          color: #fff;
          // padding: 0px 40px;
          text-transform: initial;
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 700;
          font-size: 18px;
          line-height: 25px;
          color: #ffffff;
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
              box-shadow: inset 178px 0 0 0 #0c0c0c;
              color: #ffffff;
            }
          }
        }
      }
    }
  }
}
</style>
