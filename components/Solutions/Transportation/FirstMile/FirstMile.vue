<template>
  <v-container fluid class="first-mile-main">
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-row id="first-mile">
      <div class="main_title">
        <h1>First Mile</h1>
      </div>
    </v-row>
    <v-row class="main_content">
      <v-col class="main_left_image pa-0" sm="12" md="6">
        <v-img
          class="image-jpg"
          src="/Solutions/transportation/first-mile-banner.jpg"
        />
      </v-col>

      <v-col class="main_right_content pa-0" sm="12" md="6">
        <div class="content-header">
          <h1>Make the First-Mile Count and Deliver Success From the Start</h1>
        </div>
        <div class="content-para">
          <p>
            Move material from your suppliers to processing units with ease.
            With our PTL and FTL capability spread across India, you can source
            from any part of the country and get it delivered in the stipulated
            time. We become your one-point contact and help companies avoid
            operational delays and hassle of dealing with multiple vendors.
          </p>
        </div>
        <div class="content-para-list">
          <div class="list">Pan-India Presence</div>
          <div class="list">PTL and FTL Capability</div>
          <div class="list">Intracity and Intercity Movement</div>
        </div>
        <div class="content-button">
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
.first-mile-main {
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
    background: #f3f3f5;
    padding: 0 6% !important;

    .main_left_image {
      margin: 50px 0 50px 0;
      padding-right: 58px !important;
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
          color: #1e1e1e;
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
          color: #313131;
        }
      }

      .content-para-list {
        width: 100%;
        margin-top: 1rem;
        border-left: 1px solid #313131;
        transform: rotate(0deg);

        .list {
          font-family: "Outfit";
          font-style: normal;
          font-weight: 300;
          font-size: 16px;
          line-height: 24px;
          margin-left: 1rem;
          color: #1e1e1e;
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

@media (max-width: 850px) {
  .content-header {
    h1 {
      font-size: 24px !important;
      line-height: 30px !important;
    }
  }

  .main_title {
    h1 {
      font-size: 30px !important;
    }
  }
  .first-mile-main .main_content .main_left_image {
    padding-right: 0 !important;
  }

  .first-mile-main .main_content .main_right_content {
    margin: 0 !important;
  }

  .first-mile-main .main_content .main_right_content .content-button {
    margin: 48px auto !important;
  }

  .main_content {
    flex-wrap: wrap;
    height: auto !important;

    .main_left_image,
    .main_right_content {
      .content-para {
        height: auto !important;
        padding-right: 0rem !important;
      }
      .content-button {
        position: unset !important;
      }
    }
  }
}
</style>
