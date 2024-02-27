<template>
  <v-container fluid class="middle-mile-main pt-0 pa-0">
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-row no-gutters id="first-mile">
      <div class="main_title">
        <h1>Middle Mile</h1>
      </div>
    </v-row>

    <v-row class="main_content">
      <v-col class="main_left_image pa-0" sm="12" md="6">
        <v-img
          :src="`/Solutions/transportation/middle-mile.png`"
          cover
          class="bg-grey-lighten-2 image-jpg"
        ></v-img>
      </v-col>
      <v-col class="main_right_content pa-0" sm="12" md="6">
        <div class="content-header">
          <h1>Connecting the Dots: Bridging the Gap in Your Supply Chain</h1>
        </div>
        <div class="content-para">
          <p>
            Use our Middle mile network for seamless transportation of goods and
            products between distribution centers, warehouses, and other
            intermediate locations. Access fully managed transportation
            solutions to efficiently move your goods using trucks and containers
            over long distances. In addition, our tracking and route
            optimization software ensures that your products are delivered on
            time and in the most cost-effective manner possible.
          </p>
        </div>
        <div class="content-para-list">
          <div class="list">Traceability and Fleet Management</div>
          <div class="list">Time and Cost Optimization</div>
        </div>
        <div class="content-button">
          <v-btn
            class="button bg-black"
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
.middle-mile-main {
  height: auto;

  .main_title {
    width: 100%;
    display: flex;
    background: white;
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
    }
  }

  .main_content {
    height: auto;
    background: #0c0c0c;
    padding: 0 6%;

    .main_left_image {
      margin: 50px 0 50px 0 !important;
      padding-right: 58px !important;
      padding-left: 10px !important;
    }

    .main_right_content {
      display: flex;
      flex-direction: column;
      margin: 50px 0 0 0 !important;
      position: relative;

      .content-header {
        width: 100%;

        h1 {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 300;
          font-size: 32px;
          line-height: 40px;
          color: #ffffff;
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
          color: #a3a3a3;        }
      }

      .content-para-list {
        width: 100%;
        margin-top: 1rem;
        border-left: 1px solid white;
        transform: rotate(0deg);

        .list {
          font-family: "Outfit";
          font-style: normal;
          font-weight: 300;
          font-size: 16px;
          line-height: 24px;
          margin-left: 1rem;
          color: #ffffff;
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

  .main_title {
      h1 {
      font-size: 30px !important;
      }
    }
  .middle-mile-main .main_content .main_left_image {
    padding-right: 4% !important;
    margin: 50px 0 0 0 !important;
  }
  .main_content {
    flex-wrap: wrap;
    height: auto !important;

    .main_left_content {
      margin-bottom: 20px !important;
      height: auto !important;
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

    .main_left_image,
    .main_right_content {
      height: auto !important;
      padding: 2% 2% 2% 2% !important;
      margin: 0 !important;

      .content-button {
        padding: 5% 20% !important;
        position: unset !important;
        display: flex;
        justify-content: center;
      }
    }

    img {
      width: 88vw !important;
    }
  }
}
</style>
