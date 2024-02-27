<template>
  <v-container fluid class="our-experties-container pa-0">
    <v-row no-gutters class="content-container">
      <v-col cols="12" sm="12" md="6" class="left-section-container px-0">
        <v-col class="heading px-0">
          <h2
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="800"
          >
            Embrace the Digital Age and Take Control of Your Supply Chain
          </h2>
        </v-col>
        <v-col class="sub-heading px-0">
          <span
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="900"
          >
            Streamline your operations using our consultative approach,
            operational expertise and technology. We provide flexible and
            scalable solutions that adapt as you grow.
          </span>
        </v-col>
        <HandAnimation v-if="!isSmallDevice" />
      </v-col>
      <v-col cols="12" sm="12" md="6" class="right-section-container px-0">
        <v-col
          cols="12"
          sm="12"
          md="12"
          class="item-container"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="1000"
        >
          <v-col cols="2" class="icon-container wh">
            <v-img
              src="/Homepage/OurExperties/wh-network.png"
              class="img"
              height="65px"
              contain
            >
            </v-img>
          </v-col>
          <v-col cols="10" class="content-container">
            <v-col class="title pa-0 pb-md-3">
              <h3>Warehouse Network</h3>
            </v-col>
            <v-col class="description pa-0 pa-md-3">
              <span
                >Presence Across 50+ Cities with an Extensive Network of 100+
                Warehouses and Dark Stores
              </span>
            </v-col>
          </v-col>
        </v-col>
        <v-col
          cols="12"
          class="item-container"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="1100"
        >
          <v-col cols="2" class="icon-container tc">
            <v-img
              src="/Homepage/OurExperties/tech-platform.png"
              class="img"
              height="65px"
              contain
            >
            </v-img>
          </v-col>
          <v-col cols="10" class="content-container">
            <v-col class="title pa-0 pa-md-3">
              <h3>Tech Platform</h3>
            </v-col>
            <v-col class="description pa-0 pa-md-3">
              <span
                >EdgeOS-Warehouse and Order Management System with Marketplace
                and Carrier Integration
              </span>
            </v-col>
          </v-col>
        </v-col>
        <v-col
          cols="12"
          class="item-container"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="1200"
        >
          <v-col cols="2" class="icon-container sc">
            <v-img
              src="/Homepage/OurExperties/sc.png"
              class="img"
              height="68px"
              contain
            >
            </v-img>
          </v-col>
          <v-col cols="10" class="content-container">
            <v-col class="title pa-0 pa-md-3">
              <h3>Supply Chain Expertise</h3>
            </v-col>
            <v-col class="description pa-0 pa-md-3">
              <span
                >100+ Years of Supply Chain Expertise Across Multiple Industries
              </span>
            </v-col>
          </v-col>
        </v-col>
      </v-col>

      <!-- Mobile Hand Animation -->
      <!-- Mobile End -->
      <HandAnimation v-if="isSmallDevice" />
    </v-row>
  </v-container>
</template>
<style lang="scss" scoped>
.our-experties-container {
  background-color: #0c0c0c;
  // background-image: url("/Common/background-grid-top.png");
  background-position: top;
  background-size: contain;

  .content-container {
    padding: 4% 6%;
    .left-section-container {
      .heading {
        height: auto;

        h2 {
          font-size: 42px;
          font-weight: 500;
          font-family: "Noto Serif";
          font-style: normal;
          color: #ffffff;
        }
      }

      .sub-heading {
        display: flex;
        width: 90%;
        height: 20%;
        align-items: center;
        // margin-bottom: 35px;

        span {
          font-size: 16px;
          font-weight: 300;
          color: #ffffff;
          font-family: "Outfit" !important;
        }
      }
    }

    .item-container:hover .icon-container .img {
      transform: rotate(720deg);
      transition: all 10s ease;
    }

    .right-section-container {
      .item-container {
        display: flex;
        width: 100%;
        height: auto;
        align-items: center;
        justify-content: center;
        padding: 0 10%;
        // margin-top: 90px;

      

        .icon-container {
          display: flex;
          width: 20%;
          height: auto;
          align-items: center;
          justify-content: center;
          // border: 1px solid gray;
          overflow: hidden;

          // background-image: url();

          // .img {
          //   transition: all 10s ease;

          //   &:hover {
          //     transform: rotate(720deg);
          //   }
          // }

          &.sc {
            background-image: url("/Homepage/OurExperties/person.png");
            background-position: center;
            background-size: 15%;
          }

          &.wh {
            background-image: url("/Homepage/OurExperties/whnetwork.png");
            background-position: center;
            background-size: 15%;
          }

          &.tc {
            background-image: url("/Homepage/OurExperties/techplatform_box.png");
            background-position: center;
            background-size: 15%;
          }
        }

        .content-container {
          display: flex;
          // width: 60%;
          height: auto;
          flex-direction: column;
          justify-content: center;
          // border: 1px solid gray;

          .title {
            display: flex;
            width: 100%;
            // margin-bottom: 5px;

            h3 {
              font-family: "Outfit";
              font-style: normal;
              font-weight: 500;
              font-size: 36px;
              line-height: 45px;
              color: #ffffff;
            }
          }

          .description {
            display: flex;
            width: 100%;

            span {
              font-family: "Outfit" !important;
              font-style: normal;
              font-weight: 400;
              font-size: 16px;
              line-height: 20px;

              color: #9c9c9c;
            }
          }
        }
      }
    }

    .button {
      display: flex;
      height: 42px;
      align-items: center;
      justify-content: center;
      border: 1px solid #00a699;
      border-radius: 40px;
      color: #fff;
      padding: 10px 40px;
      font-family: "Noto Serif";
      text-transform: capitalize;
      font-size: 16px;

      .v-btn__content {
        font-weight: bold;
        font-family: "Noto Serif";
      }

      &.primary {
        background-color: #00a699;

        &:hover {
          background-color: #008b80;
        }
      }

      &.secondry {
        border: 1px solid #fff;
        background-color: transparent;

        &:hover {
          border-color: #008b80;
        }
      }
    }
  }
}

@media (max-width: 850px) {
  .our-experties-container {
    display: flex !important;
    width: 100% !important;
    height: auto !important;
    background: #0c0c0c !important;
    // padding: 1.875rem 0 !important;

    .content-container {
      display: flex !important;
      width: 100% !important;
      height: 100% !important;
      align-items: center !important;
      flex-direction: column !important;
      // justify-content: space-between !important;

      .left-section-container {
        padding-right: 0rem !important;
        // padding: 4% 6% !important;

        .heading {
          // margin-bottom: 30px !important;
          // margin-top: 30px !important;
          // padding-right: 0rem !important;
          // padding: 0 10% !important;

          h2 {
            font-size: 26px !important;
            font-weight: 500 !important;
            line-height: 30px !important;
            font-family: "Noto Serif" !important;
            font-style: normal !important;
            color: #ffffff !important;
          }
        }

        .sub-heading {
          display: flex !important;
          width: 100% !important;
          justify-content: center !important;
          // margin-bottom: 0px !important;
          // padding: 0 10% 5% 10% !important;

          span {
            font-size: 14px !important;
            font-weight: 300 !important;
            line-height: 20px !important;
          }
        }
      }

      .right-section-container {
        display: flex;
        width: 100% !important;
        height: 100% !important;
        flex-direction: column;
        align-items: baseline !important;
        justify-content: flex-start !important;
        // padding: 0 6% !important;

        .item-container {
          // padding-bottom: 1rem !important;
          padding: 0 !important;

          .icon-container {
            display: flex;
            // width: 30% !important;
            height: 100% !important;
            align-items: center !important;
            justify-content: center !important;

            .img {
              width: 3rem !important;
              height: 2.3rem !important;
              transition: all 5s ease !important;

              &:hover {
                transform: rotate(720deg) !important;
              }
            }
          }

          .content-container {
            display: flex;
            width: 50% !important;
            height: 100% !important;
            flex-direction: column !important;
            justify-content: center !important;
            align-items: flex-start !important;

            .title {
              display: flex !important;
              width: 100% !important;
              // margin-bottom: 5px !important;

              h3 {
                line-height: 1.5rem !important;
                font-weight: 500 !important;
                font-size: 18.2264px !important;
              }
            }

            .description {
              display: flex !important;
              width: 100% !important;

              span {
                line-height: 0.7rem !important;
                font-weight: 400 !important;
                font-size: 2vw !important;
                // line-height: 10px !important;
              }
            }
          }
        }
      }
    }
  }
}
</style>

<script>
import aosMixin from "~/mixins/aos";
import HandAnimation from "../HandAnimation/HandAnimation.vue";

export default {
  components: {
    HandAnimation,
  },
  data() {
    return {
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
  mixins: [aosMixin],
};
</script>
