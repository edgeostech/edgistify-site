<template>
  <v-container
    fluid
    class="solutions-supportservices-container pa-0"
    id="solutions-supportservices-container"
  >
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-row no-gutters class="head-cover">
      <v-col sm="12" md="6" class="left-head-cover pa-0">
        <div class="title">
          <v-col sm="12" md="12" class="title_header pa-0 pr-md-16 pr-sm-0">
            <h1>Hassle-free Operations with Reliable Support Services</h1>
          </v-col>

          <v-col class="dashboard_content" style="padding-left: 0">
            <p>
              Reliable support services, including warehouse space,
              infrastructure, and manpower, to help you streamline your
              operations and achieve hassle-free business success.
            </p>
          </v-col>
          <v-col sm="12" md="12" class="title_button pl-md-0">
            <v-btn
              class="button bg-white"
              data-aos="fade-up"
              data-aos-once="true"
              data-aos-easing="ease-in"
              data-aos-anchor=".title"
              data-aos-anchor-placement="bottom-center"
              data-aos-duration="800"
              @click="showModal = true"
              >Get in Touch</v-btn
            >
          </v-col>
        </div>
      </v-col>
      <v-col sm="12" md="6" class="right-head-cover pa-0">
        <v-col class="head_image pa-0">
          <v-img
            :src="`/Solutions/warehousing/support-services-warehouse-management-manpower.gif.gif`"
            alt="Support services for warehouse management and manpower"
            aspect-ratio="1"
            cover
            class="bg-grey-lighten-2 image-gif"
          ></v-img>
        </v-col>
      </v-col>
    </v-row>
    <WarehouseSpace />
    <SupportServicesBenefits />
    <WarehouseInfrastructure />
    <v-row no-gutters class="empty-div">
      <v-row no-gutters class="careers-wrapper-row1">
        <v-col cols="6" sm="6" md="3" class="pr-md-6 pb-md-6 pr-3 pb-6">
          <div class="specialists-details">
            <v-img src="/Solutions/supportservices/vector1.png" class="img" />
            <div class="info-text">
              <p>Pallet </p>
            </div>
          </div>
        </v-col>
        <v-col cols="6" sm="6" md="3" class="px-md-6 pb-md-6 pl-3 pb-6">
          <div class="specialists-details">
            <v-img
              src="/Solutions/supportservices/vector2.png"
              class="img-forklifts"
            ></v-img>
            <div class="info-text">
              <p>Forklifts</p>
            </div>
          </div>
        </v-col>
        <v-col cols="6" sm="6" md="3" class="px-md-6 pb-md-6 pr-3 pb-6">
          <div class="specialists-details">
            <v-img
              src="/Solutions/supportservices/vector3.png"
              class="img-bins"
            ></v-img>
            <div class="info-text">
              <p>Bins</p>
            </div>
          </div>
        </v-col>
        <v-col cols="6" sm="6" md="3" class="pl-md-6 pb-md-6 pl-3 pb-6">
          <div class="specialists-details">
            <v-img
              src="/Solutions/supportservices/lift-table.png"
              class="img-lift-tables"
            ></v-img>
            <div class="info-text">
              <p>Lift Tables</p>
            </div>
          </div>
        </v-col>
        <v-col cols="6" sm="6" md="3" class="pr-md-6 py-md-6 pr-3 pb-6">
          <div class="specialists-details">
            <v-img
              src="/Solutions/supportservices/vector5.png"
              class="img"
            ></v-img>
            <div class="info-text">
              <p>Hydra</p>
            </div>
          </div>
        </v-col>
        <v-col cols="6" sm="6" md="3" class="px-md-6 py-md-6 pl-3 pb-6">
          <div class="specialists-details">
            <v-img
              src="/Solutions/supportservices/vector6.png"
              class="img-cctv"
            ></v-img>
            <div class="info-text">
              <p>CCTV</p>
            </div>
          </div>
        </v-col>
        <v-col cols="6" sm="6" md="3" class="px-md-6 py-md-6 pr-3">
          <div class="specialists-details">
            <v-img
              src="/Solutions/supportservices/vector7.png"
              class="img-racking"
            ></v-img>
            <div class="info-text">
              <p>Racking Systems</p>
            </div>
          </div>
        </v-col>
        <v-col cols="6" sm="6" md="3" class="pl-md-6 py-md-6 pl-3">
          <div class="specialists-details">
            <v-img
              src="/Solutions/supportservices/vector8.png"
              class="img-shelving"
            ></v-img>
            <div class="info-text">
              <p>Shelving Systems</p>
            </div>
          </div>
        </v-col>
      </v-row>
    </v-row>
    <Manpower />
    <EdgistifyForm />
  </v-container>
</template>

<script>
import aosMixin from "~/mixins/aos";
import WarehouseSpace from "../../components/Solutions/SupportServices/WarehouseSpace/WarehouseSpace.vue";
import SupportServicesBenefits from "../../components/Solutions/SupportServices/SupportServicesBenefits/SupportServicesBenefits.vue";
import WarehouseInfrastructure from "../../components/Solutions/SupportServices/WarehouseInfrastructure/WarehouseInfrastructure.vue";
import Manpower from "../../components/Solutions/SupportServices/Manpower/Manpower.vue";
import EdgistifyForm from "../../components/EdgistifyForm/EdgistifyForm.vue";
import ConnectModal from "../../components/ModalForm/ConnectModal.vue";

export default {
  components: {
    WarehouseSpace,
    SupportServicesBenefits,
    WarehouseInfrastructure,
    Manpower,
    EdgistifyForm,
    ConnectModal,
  },
  mixins: [aosMixin],
  data() {
    return {
      showModal: false,
    };
  },
  head() {
    return {
      title: "Support Services for Supply Chain Optimization and Management Ensure Success Edgistify"
    };
  }
};
</script>

<style lang="scss" scoped>
.solutions-supportservices-container {
  display: flex;
  flex-direction: column;
  width: 100%;
  height: auto;
  background-color: #0c0c0c;
  padding-top: 92px !important;

  .head-cover {
    display: flex;
    width: 100%;
    height: auto;
    align-items: center;
    justify-content: auto;
    background-color: #ffffff;

    .left-head-cover {
      display: flex;
      width: 100% !important;
      height: auto;
      background-position: center;
      background-size: contain;
      justify-content: center;

      .title {
        display: flex;
        width: 100%;
        height: 100%;
        flex-direction: column;
        justify-content: center;
        color: #1e1e1e;
        padding: 0 12%;

        .title_header {
          display: flex;
          width: 100%;

          h1 {
            font-family: "Noto Serif";
            font-style: normal;
            font-weight: 300;
            font-size: 46.61px;
            line-height: 60px;
            color: #1e1e1e;
          }
        }

        .title_button {
          display: flex;

          .button {
            display: flex;
            width: 11rem;
            height: 3rem;
            border: 1px solid #00a699;
            border-radius: 40px;
            color: #fff;
            padding: 0px 40px;
            font-family: "Noto Serif";
            text-transform: initial;
            text-transform: capitalize;
            font-size: 18px;
            font-weight: 700;
            border: none;
            letter-spacing: 0px;

            span {
              font-weight: 500 !important;
            }

            &.primary {
              background-color: #00a699;
              box-shadow: inset 0 0 0 0 #00a699;
              transition: color 0.5s ease-in-out, box-shadow 0.5s ease-in-out;

              &:hover {
                box-shadow: inset 178px 0 0 0 #000000;
                color: #ffffff;
              }
            }
          }
        }
      }
    }

    .right-head-cover {
      display: flex;
      width: 50%;
      height: 555px;

      .head_image {
        display: flex;
        width: 100%;
        height: 100%;
        margin: 0 auto;
        overflow: hidden;

        video {
          width: 100%;
          height: 100%;
          object-fit: cover;
        }
      }
    }
  }

  .empty-div {
    width: 100%;
    height: auto;
    background: #ffffff;
    padding: 6% 6%;

    .careers-wrapper-row1 {
      .specialists-details {
        // margin-bottom: 6%;
        background: #f3f3f5;
        padding: 20px;

        .img {
          width: 5rem;
          height: 4rem;
          margin-bottom: 0.5rem;
          margin: auto;
          margin-top: 50px;
        }

        .img-lift-tables {
          width: 4.3rem;
          // height: 5rem;
          margin-bottom: 0.5rem;
          margin: auto;
          margin-top: 2rem;
        }

        .img-forklifts {
          width: 5rem;
          // height: 5rem;
          margin-bottom: 0.5rem;
          margin: auto;
          margin-top: 2rem;
        }

        .img-bins {
          width: 5rem;
          // height: 5rem;
          margin-bottom: 0.5rem;
          margin: auto;
          margin-top: 2rem;
        }

        .img-racking {
          width: 5.2rem;
          // height: 5rem;
          margin-bottom: 0.5rem;
          margin: auto;
          margin-top: 2rem;
        }

        .img-shelving {
          width: 5rem;
          // height: 5rem;
          margin-bottom: 0.5rem;
          margin: auto;
          margin-top: 2rem;
        }

        .img-cctv {
          width: 6rem;
          // height: 5rem;
          margin-bottom: 0.5rem;
          margin: auto;
          margin-top: 2rem;
        }

        .info-text {
          margin: 1.5rem 0 0 0;

          p {
            font-family: "Outfit";
            font-style: normal;
            font-weight: 400;
            font-size: 16px;
            line-height: 20px;
            text-align: center;
            color: #313131;
          }
        }
      }
    }
  }
}

@media (max-width: 850px) {
  .img-cctv {
    width: 6rem !important;
  }
  .img-shelving {
    width: 4rem !important;
  }
  .solutions-supportservices-container {
    padding-top: 0 !important;
  }
  .title {
    padding-left: 0 !important;
    padding-right: 0 !important;
  }
  .title_header {
    height: auto !important;
    h1 {
      font-family: "Noto Serif" !important;
      font-style: normal !important;
      font-weight: 300 !important;
      font-size: 2rem !important;
      line-height: 2rem !important;
      color: #1e1e1e !important;
      padding-top: 30px;
      padding-left: 0 !important;
    }
  }

  .head-cover {
    flex-wrap: wrap;
    height: auto !important;
    flex-direction: column-reverse;
    padding: 0 !important;

    .right-head-cover,
    .left-head-cover {
      flex: 1 0 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      width: 100vw !important;
      height: auto !important;

      .content-para {
        margin-top: 80px !important;
        height: auto !important;
      }

      .content-header {
        height: auto !important;
      }
    }

    .left-head-cover {
      padding: 0 6% !important;
    }

    .title_header {
      padding: 0 !important;
    }

    .title_button {
      justify-content: center;
      padding: 0 20% 10% 20% !important;
    }

    .head_image {
      width: 85vw !important;
      height: 100% !important;

      video {
        width: 85vw;
      }
    }
  }
}
</style>
