<template>
  <v-container fluid class="company-container pa-0" id="careers-container">
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-row class="company-banner" no-gutters>
      <v-col sm="12" md="6">
        <div class="banner-left">
          <h1>Innovative Supply Chain Solutions that Deliver</h1>
          <div class="btn_container">
            <v-btn class="button bg-white" @click="showModal = true"
              >Schedule a call</v-btn
            >
          </div>
        </div>
      </v-col>
      <v-col sm="12" md="6">
        <div class="right-head-cover">
          <div class="head_image">
            <v-img
              :src="`/Company/innovative-supply-chain-solutions.gif.gif`"
              alt="Innovative supply chain solutions that streamline business operations"
              aspect-ratio="1"
              cover
              class="bg-grey-lighten-2 image-gif"
            ></v-img>
          </div>
        </div>
      </v-col>
    </v-row>
    <AboutUs />
    <OurJourney />
    <Vision />
    <OurAdvisors />
    <OurFounders />
    <SupplyChainSpecialists />
    <OurTeam />
  </v-container>
</template>

<script>
import AboutUs from "../../components/Company/AboutUs/AboutUs.vue";
import OurJourney from "../../components/Company/OurJourney/OurJourney.vue";
import Vision from "../../components/Company/Vision/Vision.vue";
import OurAdvisors from "../../components/Company/OurAdvisors/OurAdvisors.vue";
import OurFounders from "../../components/Company/OurFounders/OurFounders.vue";
import SupplyChainSpecialists from "../../components/Company/SupplyChainSpecialists/SupplyChainSpecialists.vue";
import OurTeam from "../../components/Company/OurTeam/OurTeam.vue";
import ConnectModal from "../../components/ModalForm/ConnectModal.vue";

export default {
  components: {
    AboutUs,
    OurJourney,
    Vision,
    OurAdvisors,
    OurFounders,
    SupplyChainSpecialists,
    OurTeam,
    ConnectModal,
  },
  data() {
    return {
      showModal: false,
    };
  },
  setup() {},
  head() {
    return {
      title: "The Leader in Supply Chain Management Edgistify"
    };
  }
};
</script>

<style lang="scss" scoped>
.company-container {
  display: flex;
  width: 100%;
  height: auto;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 0;
  padding-top: 92px !important;

  // overflow: hidden;
  .company-banner {
    width: 100%;
    display: flex;
    height: 550px;
    justify-content: center;
    align-items: center;
    background-color: #ffff;

    .banner-left {
      height: 100%;
      display: flex;
      margin: 0 12%;
      flex-direction: column;
      justify-content: center;

      h1 {
        font-family: "Noto Serif";
        font-style: normal;
        font-weight: 300;
        font-size: 46.6116px;
        line-height: 63px;
        color: #161616;
        margin-bottom: 50px;
      }

      .btn {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        padding: 11.5px 26px;
        font-family: "Noto Serif";
        gap: 10px;
        height: 48px;
        background: #00a699;
        border-radius: 38px;
        color: white;
      }
    }

    .right-head-cover {
      display: flex;
      height: 555px;

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

@media screen and (max-width: 850px) {
  .company-container {
    width: 100% !important;
    height: auto !important;
    padding-top: 0 !important;

    .company-banner {
      width: 100%;
      display: flex;
      height: auto !important;
      flex-direction: column-reverse !important;
      justify-content: center;
      align-items: center;
      background-color: #ffff;

      .banner-left {
        width: 100% !important;
        margin: 0 !important;

        h1 {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 300;
          font-size: 2rem !important;
          line-height: 2rem !important;
          color: #161616;
          margin: 30px !important;
        }

        .btn_container {
          margin: 30px auto;
        }

        .btn {
          padding: 0px 0px !important;
          width: 11.5rem !important;
          height: 2.438rem !important;
          border-radius: 1.938rem !important;
          margin: 0 auto !important;
        }
      }

      .right-head-cover {
        display: flex;
        width: 100% !important;
        height: 355px !important;

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
}
</style>
