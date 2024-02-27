<template>
  <v-container fluid class="warehouse-infrastructure-main pa-0">
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-row no-gutters class="main_title" id="warehouse-infra">
      <h1>Warehouse Infrastructure</h1>
    </v-row>
    <v-row no-gutters class="main_content">
      <v-col class="main_left_content" md="6" sm="12">
        <div class="content-header pl-0" md="6">
          <h1>Best-in-Class Warehouse Infrastructure</h1>
        </div>
        <div class="main_right_image pl-0" v-if="isSmalldevice">
          <v-img
            :src="`/Solutions/supportservices/integrated-warehousing-solutions.jpg.jpg`"
            alt="Integrated Warehousing Solutions for streamlined supply chain management"
            contain
            class="bg-grey-lighten-2 image-jpg"
          ></v-img>
        </div>
        <div class="content-para pl-0 pr-md-16">
          <p>
            Get access to a wide range of storage alternatives and material
            handling equipment to meet the physical and operational requirements
            of the warehouse. In addition, our warehouse infra solutions have
            optimal automation that ensures smooth operations, reduced
            dependency on manpower and optimization at every level.
          </p>
        </div>
        <div class="content-button">
          <v-btn
            class="button bg-black"
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="1000"
            data-aos-anchor=".content-para"
            @click="showModal = true"
            >Schedule a call</v-btn
          >
        </div>
      </v-col>
      <v-col class="main_right_image" md="6" sm="12" v-if="!isSmalldevice">
        <v-img
          :src="`/Solutions/supportservices/integrated-warehousing-solutions.jpg.jpg`"
          alt="Integrated Warehousing Solutions for streamlined supply chain management"
          contain
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
.warehouse-infrastructure-main {
  .image-jpg {
    height: 24.625rem !important;
  }

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
    // width: 100%;
    height: auto;
    // display: flex;
    background: #0c0c0c;
    padding: 6% 6%;

    .main_left_content {
      display: flex;
      flex-direction: column;
      // width: 50%;
      // margin: 80px 0 0 100px;
      height: auto;
      position: relative;

      .content-header {
        // width: 100%;
        height: auto;

        h1 {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 300;
          font-size: 32px;
          line-height: 44px;
          color: #ffffff;
        }
      }

      .content-para {
        // width: 100%;
        height: auto;
        margin-top: 1rem;

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
          width: 11rem;
          height: 3rem;
          border: 0px solid #00a699;
          border-radius: 73px;
          color: #fff;
          // padding: 0px 40px;
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
              box-shadow: inset 178px 0 0 0 #ffffff;
              color: #000000;
            }
          }
        }
      }
    }

    .main_right_image {
      // margin: 80px 7% 0 0;
      // width: 582px;
      height: auto;

      img {
        // width: 100%;
        height: 100%;
      }
    }
  }
}

@media (max-width: 850px) {
  .warehouse-infrastructure-main .image-jpg {
    height: auto !important;
  }
  .warehouse-infrastructure-main {
    .main_title {
      padding: 0 6% !important;

      h1 {
        font-size: 30px !important;

      }
    }

    .main_content {
      flex-wrap: wrap;
      height: auto !important;
      flex-direction: column-reverse;
      padding: 0 6% !important;

      .main_left_content {
        margin-bottom: 20px !important;
        height: auto !important;

        .content-button {
          padding: 5% 20% !important;
          position: unset !important;
          display: flex;
          justify-content: center;
        }
      }

      .content-para {
        height: auto !important;
      }

      .content-header {
        height: auto !important;
        h1 {
          padding: 4% 0 !important;
          font-size: 24px !important;
          line-height: 30px !important;

        }
      }

      .main_left_content,
      .main_right_image {
        height: auto !important;
      }

      img {
        width: 88vw !important;
        height: 100%;
      }
    }
  }
}
</style>
