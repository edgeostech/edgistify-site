<template>
  <v-container
    fluid
    class="solutions-supportservices-container pa-0"
    id="solutions-supportservices-container"
  >
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-row no-gutters class="head-cover">
      <v-col class="left-head-cover" sm="12" md="6">
        <v-col class="title px-0">
          <v-col class="title_header px-0">
            <h1>Maximize Efficiency with Our Supply Chain Expertise</h1>
          </v-col>

          <v-col class="dashboard_content">
            <p>
              Unlock the full potential of your supply chain with over 100 years
              of expertise. Increase efficiency and reduce costs with our
              tailored solutions. Book a free 30-minute consultation today.
            </p>
          </v-col>

          <div class="title_button">
            <v-btn
              class="button bg-white"
              data-aos="fade-up"
              data-aos-once="true"
              data-aos-easing="ease-in"
              data-aos-anchor=".content-para"
              data-aos-duration="1000"
              @click="showModal = true"
              >Schedule a call</v-btn
            >
          </div>
        </v-col>
      </v-col>
      <v-col class="right-head-cover pa-0" sm="12" md="6">
        <v-col class="head_image pa-0">
          <v-img
            :src="`/Solutions/warehousing/consulting-supply-chain.gif`"
            alt=""
            aspect-ratio="1"
            cover
            class="bg-grey-lighten-2 image-gif"
          ></v-img>
        </v-col>
      </v-col>
    </v-row>
    <SupplyChain />
    <AreasOfWork />
    <OurIndustries />

    <Form />
    <TrustedBy />
  </v-container>
</template>

<script>
import aosMixin from "~/mixins/aos";
import SupplyChain from "../../components/Solutions/Consulting/SupplyChain/SupplyChain.vue";
import AreasOfWork from "../../components/Solutions/Consulting/AreasOfWork/AreasOfWork.vue";
import OurIndustries from "../../components/Solutions/Consulting/OurIndustries/OurIndustries.vue";
import Form from "../../components/Solutions/Consulting/Form.vue";
import TrustedBy from "../../components/Solutions/Consulting/TrustedBy/TrustedBy.vue";
import ConnectModal from "../../components/ModalForm/ConnectModal.vue";
export default {
  components: {
    SupplyChain,
    AreasOfWork,
    OurIndustries,
    ConnectModal,

    Form,
    TrustedBy,
  },
  mixins: [aosMixin],

  data() {
    return {
      showModal: false,
    };
  },
  head() {
    return {
      title: "Maximizing Efficiency and Reducing Costs Consulting of Supply Chain Management Edgistify"
    };
  }
};
</script>

<style lang="scss" scoped>


.solutions-supportservices-container {
  height: auto;
  background-color: #0c0c0c;
  padding-top: 92px !important;

  .head-cover {
    height: auto;
    background: #ffffff;

    .left-head-cover {
      height: auto;
      background-position: center;
      background-size: contain;
      justify-content: center;
      padding: 4% 0 0 6%;

      .title {
        height: auto;
        color: #1e1e1e;

        .title_header {
          width: 100%;

          h1 {
            font-family: "Noto Serif";
            font-style: normal;
            font-weight: 300;
            font-size: 46.61px;
            line-height: 60px;
            color: #1e1e1e;
          }

          h2 {
            font-family: "Outfit";
            font-style: normal;
            font-weight: 300;
            font-size: 20px;
            line-height: 25px;
            color: #313131;
          }
        }

        .title_button {
          display: flex;

          .button {
            display: flex;
            height: 48px;
            width: 178px;
            border: 1px solid #00a699;
            border-radius: 40px;
            color: #fff;
            font-family: "Noto Serif";
            text-transform: capitalize;
            font-size: 18px;
            font-weight: 700;

            span {
              font-weight: 500 !important;
            }

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

    .right-head-cover {
      height: auto;

      .head_image {
        height: auto;
        margin: 0 auto;
        overflow: hidden;
        background: #0c0c0c;

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
    height: 600px;
    background: #ffffff;
  }
}
@media (max-width: 850px) {
  .solutions-supportservices-container {
  padding-top: 0 !important;}
  .left-head-cover {
    margin: 0 !important;
    padding: 0 6% !important;

    .title {
      // padding-left: 20px !important;
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
      }
    }

    .title_button {
      display: flex !important;
      padding: 0 20% 10% 20% !important;
      justify-content: center;

      .button {
        font-size: 14px !important;
      line-height: 20px !important;
      font-weight: 300 !important;
        span {
          font-weight: 300 !important;
        }

        &.primary {
          background-color: #00a699 !important;
          box-shadow: inset 0 0 0 0 #00a699 !important;
          transition: color 0.3s ease-in-out, box-shadow 0.3s ease-in-out !important;
        }
      }
    }
  }

  .head-cover {
    height: auto !important;
    flex-direction: column-reverse !important;

    .right-head-cover,
    .left-head-cover {
      height: auto !important;

      .content-para {
        margin-top: 80px !important;
        height: auto !important;
      }

      .content-header {
        height: auto !important;
      }
    }

    .head_image {
      height: 100% !important;

      video {
        width: 85vw;
      }
    }
  }
}
</style>
