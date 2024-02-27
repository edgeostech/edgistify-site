<template>
  <v-container fluid class="manpower-main pa-0 pt-md-3">
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-row no-gutters id="manpower">
      <div class="main_title">
        <h1>Manpower</h1>
      </div>
    </v-row>
    <v-row no-gutters class="main_content">
      <v-col class="main_left_image pr-md-16" sm="12" md="6">
        <div class="main_right_image pl-0">
          <v-img
            :src="`/Solutions/supportservices/manpower-banner.png`"
            contain
            class="bg-grey-lighten-2"
          ></v-img>
        </div>
      </v-col>
      <v-col class="main_right_content" sm="12" md="6">
        <div class="content-header px-0">
          <h1>Skilled Workforce to Achieve Operational Excellence</h1>
        </div>
        <div class="content-para">
          <p>
            Find perfectly matched candidates suitable for your Supply Chain
            requirements. Deploy manpower resources for long-term contracts
            lasting for years and short-term contracts for a few weeks or
            months. We enable our clients to focus on their core business
            strategies while transferring the efforts and risk of hiring,
            training and deploying manpower to us. Our resource pool is verified
            and skilled, which ensures stress-free operations. Our 360-degree
            manpower solutions allow you to deploy warehouse assistants,
            loaders, sorters, scanners, packers, MHE operators, and data entry
            technicians as per your needs.
          </p>
        </div>
        <div class="content-button">
          <v-btn
            class="button bg-white"
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="1000"
            data-aos-anchor=".content-para"
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

.manpower-main {
  height: auto;
  background: #ffffff;
  .main_title {
    width: 100%;
    display: flex;
    background: #00a699;
    justify-content: baseline;
    align-items: center;
    padding: 0 6%;

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
    padding: 4% 6%;

    .main_left_image {
      height: auto;
    }

    .main_right_content {
      height: auto;
      position: relative;
      margin-top: -8px;

      .content-header {
        height: auto;

        h1 {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 300;
          font-size: 32px;
          line-height: 40px;
          color: #1e1e1e;
        }
      }

      .content-para {
        height: auto;
        padding: 5% 0;

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
        margin: 5% 0 0 0;
        position: absolute;
        bottom: 0;

        .button {
          display: flex;
          width: 11rem;
          height: 3rem;
          border-radius: 73px;
          color: #fff;
          text-transform: capitalize;
          font-family: "Noto Serif";
          text-transform: capitalize;
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

@media (max-width: 850px) { 

  .main_right_image {
    padding: 6% 0 !important;
  }
  .main_title {
    width: 100%;
    display: flex;
    background: #00a699;
    justify-content: baseline;
    align-items: center;
    padding: 0 6%;

    h1 {
      font-size: 30px !important;
    }
  }
  .main_content {
    height: auto !important;
    padding: 0 6% !important;

    .content-para {
      height: auto !important;
      padding: 3% 0 !important;
    }

    .content-header {
      height: auto !important;
      padding: 3% 0 !important;
      h1 {
        font-size: 24px !important;
        line-height: 30px !important;
      }
    }

    .main_left_image,
    .main_right_content {
      height: auto !important;
    }

    .content-button {
      margin: 0 !important;
      padding: 5% 20% !important;
      position: unset !important;
      justify-content: center;
    }

    img {
      width: 88vw !important;
      height: 100%;
    }
  }
}


</style>
