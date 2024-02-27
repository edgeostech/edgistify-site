<template>
  <v-container fluid class="homepage-container pa-0">
    <Connectmodal v-show="showModal" @close-modal="showModal = false" />
    <!-- <img src="~/assets/Header_imag.png" :bg="true"/> -->
    <!-- <particles-bg type="cobweb" :bg="true" color="#ffffff"/> -->
    <v-row no-gutters class="hero-container">
      <v-col cols="12" class="video-box">
        <!-- <video class="video-heading" autoplay="false" muted loop>
          <source
            src="https://edgistify.s3.ap-south-1.amazonaws.com/media/website2023_video/website_video.mp4"
            type="video/mp4"
          />
        </video> -->

        <v-img :src="`/Solutions/warehousing/supply-chain-management-edgistify.gif.gif`"

          alt="Optimized supply chain management through Edgistify's technology solutions" cover
          class="video-heading"></v-img>
      </v-col>
      <v-col cols="12" class="title">
        <v-col class="heading-title px-0">
          <h1>
            Superfast <b> <span> Same Day</span></b> <br />
            <b><span>Delivery</span> Pan India</b>
          </h1>
          <h1>
            An <b><span>Integrated Supply</span></b> <br />
            <b> <span> Chain </span></b>
            <b> Solutions Provider</b>
          </h1>
          <h1>
            Scalable <b> <span> Fulfillment and</span></b> <br />
            <b><span>Warehousing</span> Operations</b>
          </h1>
          <h1>
            Superfast <b> <span> Same Day</span></b> <br />
            <b><span>Delivery</span> Pan India</b>
          </h1>
        </v-col>

        <v-col class="heading-container mt-4 px-0">
          <h2 classs="h2">
            Edgistify offers Integrated Supply Chain Solutions for B2B and B2C companies across different industries
          </h2>

          <v-col class="heading-btn px-0">
            <v-btn class="button bg-black" data-aos="fade-up" data-aos-once="true" data-aos-easing="ease-in"
              data-aos-anchor=".heading-container" data-aos-duration="100" @click="showModal = true">
              Schedule a Call</v-btn>
          </v-col>
        </v-col>
      </v-col>
    </v-row>
    <v-row no-gutters class="contact-container" v-if="!isSmallDevice">
      <v-col cols="12" class="heading-container">
        <v-col cols="2" class="heading heading-1">
          <h2>1 Lac<span>+</span></h2>
          <span data-aos="zoom-out" data-aos-once="true" data-aos-easing="ease-in" data-aos-duration="600"
            data-aos-anchor=".heading-btn">Daily Orders</span>
        </v-col>
        <v-col cols="2" class="heading heading-2">
          <h2>75<span>+</span></h2>
          <span data-aos="zoom-out" data-aos-once="true" data-aos-easing="ease-in" data-aos-anchor=".heading-btn"
            data-aos-duration="700">Integrations</span>
        </v-col>
        <v-col cols="2" class="heading heading-3">
          <h2>50<span>+</span></h2>
          <span data-aos="zoom-out" data-aos-once="true" data-aos-easing="ease-in" data-aos-duration="800"
            data-aos-anchor=".heading-btn">Cities</span>
        </v-col>
        <v-col cols="2" class="heading heading-4">
          <h2>100<span>+</span></h2>
          <span data-aos="zoom-outt" data-aos-once="true" data-aos-easing="ease-in" data-aos-anchor=".heading-btn"
            data-aos-duration="900">Warehouses</span>
        </v-col>
        <v-col cols="2" class="heading heading-5">
          <h2>50<span>+</span></h2>
          <span data-aos="zoom-out" data-aos-once="true" data-aos-easing="ease-in" data-aos-anchor=".heading-btn"
            data-aos-duration="1000">Customers</span>
        </v-col>
      </v-col>
      <!-- <v-col cols="12" class="description-container">
        <v-img src="/service_high.png"></v-img>

        <div class="floating-text">
          <span id="ft"
            >A Perfect Blend of Technology and Operational Excellence
          </span>
        </div>
      </v-col> -->
    </v-row>
    <!-- Mobile Layout -->
    <v-row no-gutters class="contact-container" v-if="isSmallDevice">
      <v-col cols="12" class="heading-container">
        <v-col class="heading heading-1">
          <h2>1 Lac<span>+</span></h2>
          <span data-aos="zoom-out" data-aos-once="true" data-aos-easing="ease-in" data-aos-duration="600"
            data-aos-anchor=".heading-btn">Daily Orders</span>
        </v-col>
        <v-col class="heading heading-2">
          <h2>75<span>+</span></h2>
          <span data-aos="zoom-out" data-aos-once="true" data-aos-easing="ease-in" data-aos-anchor=".heading-btn"
            data-aos-duration="700">Integrations</span>
        </v-col>
        <v-col class="heading heading-3">
          <h2>50<span>+</span></h2>
          <span data-aos="zoom-out" data-aos-once="true" data-aos-easing="ease-in" data-aos-duration="800"
            data-aos-anchor=".heading-btn">Cities</span>
        </v-col>
      </v-col>
      <v-col cols="12" class="heading-container1">
        <v-col class="heading heading-4">
          <h2>100<span>+</span></h2>
          <span data-aos="zoom-outt" data-aos-once="true" data-aos-easing="ease-in" data-aos-anchor=".heading-btn"
            data-aos-duration="900">Warehouses</span>
        </v-col>
        <v-col class="heading heading-5">
          <h2>50<span>+</span></h2>
          <span data-aos="zoom-out" data-aos-once="true" data-aos-easing="ease-in" data-aos-anchor=".heading-btn"
            data-aos-duration="1000">Customers</span>
        </v-col>
      </v-col>
      <v-col cols="12" class="description-container">
        <!-- <img src="/service_high_mob.png" />
        <div class="floating-text">
          <span id="ft"
            >A Perfect Blend of Technology and Operational Excellence
          </span>
        </div> -->
        <v-btn class="button primary contact-us" data-aos="fade-up" data-aos-once="true" data-aos-easing="ease-in"
          data-aos-duration="1000">Contact us</v-btn>
      </v-col>
    </v-row>
    <!-- Mobile End -->
    <TrustedBrands />
    <OurMessage />
    <OurServices />
    <OurNetworks />
    <OurExperties />
    <!-- <HandAnimation /> -->
    <!-- <OurAwards /> -->
    <OurReach />
    <OurStories />
    <OurPresence />
    <!-- <Testimonials /> -->
    <OurInsights />
    <EdgistifyForm />
  </v-container>
  <!-- <v-navigation-drawer>
    v-model="vm_orderDetail_DLG"
    right
    temporary
    class="rightNavDrawerCustom"
  </v-navigation-drawer> -->
</template>

<style lang="scss" scoped>
@media (max-width: 850px) {
  // .hidden-mobile {
  //   display: none !important;
  // }


  .hero-container {
    min-height: 50vh !important;
    }  .homepage-container {
    height: auto !important;
    overflow-x: clip !important;
    // width: 100% !important;
    // max-width: 100% !important;
    // overflow-x: hidden !important;

    .contact-us {
      display: none !important;
    }

    .floating-text {
      span {
        white-space: nowrap !important;
        font-size: 24px !important;
      }
    }

    .contact-container {
      height: auto !important;
      width: 100% !important;
      background-color: #fff !important;

      .heading-container {
        display: flex !important;
        flex-wrap: wrap !important;
        height: 100% !important;

        .heading {
          height: 40% !important;
          flex: 1 0 80px !important;
          margin: 0px !important;
          display: flex !important;
          align-items: center !important;
          justify-content: center !important;
          border-left: 1px solid #8d8d8d !important;

          &:nth-child(3) {
            border-right: 1px solid #8d8d8d !important;
          }

          &:last-child {
            border-right: 1px solid #8d8d8d !important;
          }

          h2 {
            font-family: "Noto Serif" !important;
            font-style: normal !important;
            font-weight: 600 !important;
            font-size: 24.5603px !important;
            line-height: 33px !important;
            color: #1e1e1e !important;

            span {
              font-weight: 600 !important;
              font-size: 25px !important;
              line-height: 33px !important;
              color: #00a699 !important;
            }
          }

          span {
            margin-top: 5% !important;
            font-family: "Outfit" !important;
            font-style: normal !important;
            font-weight: 350 !important;
            font-size: 12px !important;
            line-height: 8px !important;
            color: #1e1e1e;
          }
        }
      }

      .heading-container1 {
        display: flex !important;
        flex-wrap: wrap !important;
        width: 60% !important;
        padding: 6% 0 !important;

        .heading {
          height: 40% !important;
          flex: 1 0 40px !important;
          margin: 0px !important;
          display: flex !important;
          align-items: center !important;
          flex-direction: column !important;
          justify-content: center !important;
          border-left: 1px solid #8d8d8d !important;

          &:nth-child(2) {
            border-right: 1px solid #8d8d8d !important;
          }

          &:last-child {
            border-right: 1px solid #8d8d8d !important;
          }

          h2 {
            font-family: "Noto Serif" !important;
            font-style: normal !important;
            font-weight: 600 !important;
            font-size: 24.5603px !important;
            line-height: 33px !important;
            color: #1e1e1e !important;

            span {
              font-weight: 600 !important;
              font-size: 25px !important;
              line-height: 33px !important;
              color: #00a699 !important;
            }
          }

          span {
            margin-top: 5% !important;
            font-family: "Outfit" !important;
            font-style: normal !important;
            font-weight: 350 !important;
            font-size: 12px !important;
            line-height: 8px !important;
            color: #1e1e1e;
          }
        }
      }

      .description-container {
        img {
          height: 12.188rem !important;
        }
      }
    }
  }
}

.homepage-container {
  height: auto;
  background-color: #000000;

  .hero-container {
    height: auto;
    position: relative;
    min-height: 100vh;

    .video-heading {
      height: auto;
      width: 100%;
      object-fit: cover;
    }

    .title {
      position: absolute;
      height: auto;
      padding: 10% 0 5% 6%;

      .heading-title {
        position: relative;
        height: 9.375rem;
        overflow: hidden;
        padding: 0;

        h1 {
          font-size: 3.125rem;
          font-weight: 600;
          font-family: "Noto Serif";
          position: relative;
          line-height: 4.256rem;
          animation: infinite slide-top 10s linear;
          color: #ffffff;

          @keyframes slide-top {
            0% {
              transform: translateY(0%);
            }

            20% {
              transform: translateY(0%);
            }

            30% {
              transform: translateY(-100%);
            }

            50% {
              transform: translateY(-100%);
            }

            60% {
              transform: translateY(-200%);
            }

            80% {
              transform: translateY(-200%);
            }

            90% {
              transform: translateY(-300%);
            }

            100% {
              transform: translateY(-300%);
            }
          }

          b {
            font-weight: 600;
            font-size: 3.125rem;
            font-family: "Noto Serif";

            span {
              color: #00a699;
            }
          }
        }
      }

      .heading-container {
        display: flex;
        // margin-top: 1rem;
        align-items: left;
        justify-content: center;
        flex-direction: column;
        width: 40%;
        height: auto;
        position: relative;

        h2 {
          font-size: 1rem;
          font-weight: 100;
          font-family: "Outfit";
          font-style: normal;
          line-height: 20.16px;
          color: #a3a3a3;

          b {
            font-weight: 400;
            font-size: 1rem;
            font-family: "outfit";
            font-style: normal;
          }
        }

        span {
          font-family: "Outfit";
          font-style: normal;
        }

        .heading-btn {
          display: flex;
          margin-top: 4.063rem;
        }
      }
    }
  }

  .action {
    display: flex;
    width: 100%;
    height: 100%;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;

    .slide-items {
      display: flex;
      width: 120%;
      align-items: center;
      border-top: 2px solid #ffffff;
      border-bottom: 2px solid #ffffff;
      height: 40px;
      overflow: hidden;
      text-transform: uppercase;
      position: relative;
      transition: all 0.5s ease;
      background-color: black;
      // z-index: 1;

      div {
        display: inline-block;
        position: absolute;
        overflow: hidden;
        height: 20px;

        animation: marquee 50s linear infinite;

        span {
          padding: 0 1rem;
          font-size: 14px;
          float: left;
          overflow: hidden;
          color: #fff;
          font-weight: 300;
        }

        .dot {
          color: #00a699;
        }
      }
    }

    @keyframes marquee {
      0% {
        left: 10%;
      }

      100% {
        left: -100%;
      }
    }
  }

  .contact-container {
    height: auto;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    background-color: #0c0c0c;

    .heading-container {
      display: flex;
      width: 100%;
      height: auto;
      align-items: center;
      background-color: #fff;
      padding: 2% 6%;
      justify-content: space-between;
      // z-index: 1;

      .heading-1 {
        border-left: 1px solid #8d8d8d;
      }

      .heading-5 {
        border-right: 1px solid #8d8d8d;
      }

      .heading {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        color: #0c0c0c;
        border-left: 1px solid #8d8d8d;

        // &:first-child {
        //   border: none;
        // }

        span {
          font-family: "Outfit";
          font-size: 16px;
          font-weight: 400;
        }

        h2 {
          font-family: "Noto Serif";
          font-size: 2.813rem;
          font-weight: 500;

          span {
            font-size: 2.813rem;
            color: #00a699;
          }
        }
      }
    }

    .description-container {
      height: auto;
      justify-content: center;
      background-position: center;
      background-size: contain;
      overflow: hidden;

      .button {
        margin-top: 10%;
      }

      img {
        width: 120%;
        height: 400px;
      }

      .floating-text {
        position: absolute;
        display: flex;
        width: 200%;
        align-items: center;
        justify-content: center;
        top: 35%;

        // z-index: 1;

        span {
          transition: all 0.6s ease;
          animation: marquee 30s linear infinite;
          justify-content: center;
          position: relative;
          font-size: 82px;
          font-weight: 500;
          font-family: "Noto Serif";
          color: #ffffff;
          left: 90vw;
        }
      }

      position: relative;
      overflow: hidden;

      video {
        position: absolute;
        align-content: center;

        width: 100%;
        height: auto;
      }
    }
  }

  @keyframes marquee {
    0% {
      left: 10%;
    }

    100% {
      left: -100%;
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
    font-size: 16px;
    font-weight: 800;
    border: none;
    letter-spacing: 0px;

    // .v-btn__content {
    //   font-weight: bold;
    //   font-family: "Noto Serif";
    // }

    span {
      font-weight: 500 !important;
    }

    &.primary {
      background-color: #00a699;
      box-shadow: inset 0 0 0 0 #00a699;
      transition: color 0.3s ease-in-out, box-shadow 0.3s ease-in-out;

      &:hover {
        background-color: #008b80;
        box-shadow: inset 230px 0 0 0 #ffffff;
        color: #0c0c0c;
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

@media (max-width: 850px) {
  .homepage-container {
    width: 100% !important;
    max-width: 100% !important;
    // touch-action: none !important;

    .hero-container {
      .video-box {
        padding-top: 42%;

      }

      .video-heading {
        width: 100% !important;
      }

      .title {
        padding: 10% 0 0 5% !important;

        .heading-title {
          height: 75px !important;
          overflow: hidden;

          h1 {
            font-size: 28px !important;
            // font-weight: 200 !important;
            line-height: 35px !important;
            animation: infinite slide-top 8s linear !important;

            padding-bottom: 16px !important;

            // @keyframes slide-top {
            //   0% {
            //     transform: translateY(0%);
            //   }

            //   20% {
            //     transform: translateY(-60%);
            //   }

            //   40% {
            //     transform: translateY(-120%);
            //   }

            //   60% {
            //     transform: translateY(-180%);
            //   }

            //   80% {
            //     transform: translateY(-240%);
            //   }

            //   100% {
            //     transform: translateY(-300%);
            //   }
            // }

            b {
              font-size: 28px !important;
            }

            b {
              font-size: 28px !important;

              span {
                font-size: 28px !important;
              }
            }
          }
        }

        .heading-container {
          width: 100%;
          height: 150px;
          position: relative;
          padding-right: 6% !important;

          // height: 90px !important;
          h2 {
            // color: #fff;
            font-size: 16px !important;
            font-weight: 100 !important;
            line-height: 20px !important;

            b {
              font-size: 16px !important;
            }
          }

          .heading-btn {
            margin-top: 2rem !important;
          }
        }
      }
    }

    .button {
      height: 2rem !important;
      width: 8rem !important;
      font-size: 14px !important;
      line-height: 20px !important;
      font-weight: 300 !important;
    }

    .action {
      .slide-items {
        border-top: 1px solid #ffffff;
        border-bottom: 1px solid #ffffff;
        height: 25px;
        transition: all 0.5s ease;

        div {
          height: 15px;
          animation: marquee 10s linear infinite;
          align-items: center;

          span {
            padding: 0 0.5rem;
            font-size: 10px;
            font-weight: 200;
          }

          .dot {
            color: #00a699;
          }
        }
      }

      @keyframes marquee {
        0% {
          left: 10%;
        }

        100% {
          left: -100%;
        }
      }
    }
  }
}
</style>

<script>
import TrustedBrands from "../components/HomePage/TrustedBrands/TrustedBrands.vue";
import OurMessage from "../components/HomePage/OurMessage/OurMessage.vue";
import OurServices from "../components/HomePage/OurServices/OurServices.vue";
import OurNetworks from "../components/HomePage/OurNetwork/OurNetworks.vue";
import OurExperties from "../components/HomePage/OurExperties/OurExperties.vue";
import HandAnimation from "../components/HomePage/HandAnimation/HandAnimation.vue";
import OurAwards from "../components/HomePage/OurAwards/OurAwards.vue";
import OurReach from "../components/HomePage/OurReach/OurReach.vue";
import OurStories from "../components/HomePage/OurStories/OurStories.vue";
import OurInsights from "../components/HomePage/OurInsights/OurInsights.vue";
import OurPresence from "../components/HomePage/OurPresence/OurPresence.vue";
import Testimonials from "../components/HomePage/Testimonials/Testimonials.vue";
import Connectmodal from "../components/ModalForm/ConnectModal.vue";
import EdgistifyForm from "../components/EdgistifyForm/EdgistifyForm.vue";
import aosMixin from "~/mixins/aos";

export default {
  components: {
    TrustedBrands,
    OurServices,
    OurNetworks,
    OurExperties,
    OurAwards,
    OurReach,
    OurStories,
    OurPresence,
    Testimonials,
    OurInsights,
    OurMessage,
    HandAnimation,
    Connectmodal,
    EdgistifyForm,
  },
  data () {
    return {
      showModal: false,
      isSmallDevice: false,
    };
  },
  mixins: [aosMixin],
  mounted () {
    window.addEventListener("scroll", this.onScroll);
    if (window.innerWidth <= 850) {
      this.isSmallDevice = true;
    } else {
      this.isSmallDevice = false;
    }
  },
  beforeDestroy () {
    window.removeEventListener("scroll", this.onScroll);
  },
  methods: {
    onScroll (e) {
      if (window.top.scrollY < 400) {
        document.querySelector("#ft").style.left = "125vw";
      }

      if (window.top.scrollY > 400 && window.top.scrollY < 800) {
        document.querySelector("#ft").style.left = "0vw";
      }

      if (window.top.scrollY > 800) {
        document.querySelector("#ft").style.left = "-125vw";
      }
    },
  },
};
</script>
