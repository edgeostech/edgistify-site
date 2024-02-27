<template>
  <v-container fluid class="warehouse-space-main pa-0">
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-row no-gutters class="main_title" id="warehouse-space">
      <h1>Design. Execute. Optimize.</h1>
    </v-row>
    <v-row no-gutters class="main_content">
      <v-col class="main_left_image pr-md-16" sm="12" md="6">
        <v-img
          :src="`/Solutions/supportservices/warehouse-spce-banner.png`"
          contain
          class="bg-grey-lighten-2 image-jpg"
        ></v-img>
      </v-col>
      <v-col class="main_right_content" sm="12" md="6">
        <v-col class="content-para px-0">
          <p>
            Supply Chain redesign can help you seize a competitive advantage. We
            help companies design their supply chain to align with their
            business strategy. Our service model is designed to take a holistic
            approach  that enables end to end systems integration to have a
            complete visibility and to ensure your supply chain capabilities
            continuously adapt to meet evolving business requirements or
            changing market needs.
          </p>
        </v-col>
        <v-col class="content-para-list pa-0">
          <div class="list">Industry Specific Team of Experts</div>
          <div class="list">Collaborative Approach</div>
          <div class="list">Integrated Solutions</div>
          <div class="list">Experience of Optimizing Complex Supply Chain</div>
        </v-col>
        <v-col class="content-button">
          <v-btn
            class="button bg-white"
            @click="showModal = true"
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="1000"
            >Get in Touch</v-btn
          >
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
      showModal: false,
    };
  },
};
</script>

<style lang="scss" scoped>
@media (max-width: 850px) {
  .main_title {
    h1 {
      font-weight: 500 !important;
      font-size: 30px !important;
      line-height: 2rem !important;
    }
  }

  .main_content {
    height: auto !important;

    .content-para {
      height: auto !important;
    }

    .main_left_image,
    .main_right_content {
      height: auto !important;

      .content-button {
        padding: 10% 20% !important;
        position: unset !important;
        justify-content: center;

        .button {
          font-size: 14px !important;
          line-height: 20px !important;
          font-weight: 300 !important;

          span {
            font-weight: 500 !important;
          }
        }
      }
    }

    img {
      width: 85vw !important;
      height: 100% !important;
    }
  }
}

.warehouse-space-main {
  height: auto;

  .main_title {
    // height: 110px;
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
      color: #ffffff;
    }
  }

  .main_content {
    // width: 100%;
    height: auto;
    // display: flex;
    background: #ffffff;
    padding: 4% 6%;

    .main_left_image {
      // margin: 80px 45px 0 100px;
      // width: 50%;
      height: auto;
    }

    .main_right_content {
      height: auto;
      position: relative;

      .content-para {
        height: auto;

        p {
          font-family: "Outfit";
          font-style: normal;
          font-weight: 300;
          font-size: 1rem;
          line-height: 20px;
          color: #313131;
        }
      }

      .content-para-list {
        border-left: 1px solid #313131;
        transform: rotate(0deg);
        height: auto;

        .list {
          padding-top: 0.5rem;
          font-family: "Outfit";
          font-style: normal;
          font-weight: 300;
          font-size: 1rem;
          line-height: 24px;
          margin-left: 1rem;
          color: #000000;
        }
      }

      .content-button {
        display: flex;
        padding: 6% 0 0 0;
        position: absolute;
        bottom: 0;

        .button {
          display: flex;
          height: 40px;
          width: 170px;
          border-radius: 73px;
          color: #fff;
          font-family: "Noto Serif";
          text-transform: capitalize;
          font-style: normal;
          font-size: 14px;
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
