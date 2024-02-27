<template>
  <v-container fluid class="our-presence-container">
    <div class="heading-container">
      <h2 data-aos="fade-up" data-aos-once="true" data-aos-easing="ease-in" data-aos-duration="800">
        Pan-India Network Serving 18000+ Pin Codes
      </h2>
    </div>
    <v-row no-gutters class="content-container">
      <v-col class="map-container" md="6">
        <img src="/Homepage/cities.gif" cover class="thread1" ref="threeds" />

        <img :src="`/Homepage/pan.gif`" aspect-ratio="1" cover class="thread2" ref="tier" />
        <img :src="`/Homepage/warehouses.gif`" aspect-ratio="1" cover class="thread3" ref="twohundwh" />
        <img :src="`/Homepage/area managed.gif`" aspect-ratio="1" cover class="thread4" ref="allmetro" />
        <!-- <video class="thread1" ref="threeds" src="https://edgistify.s3.ap-south-1.amazonaws.com/media/website2023_video/threeds.mp4" type="video/mp4" loop muted></video> -->
        -->
        <!-- <video class="thread2" ref="tier" src="https://edgistify.s3.ap-south-1.amazonaws.com/media/website2023_video/tier.mp4" type="video/mp4" loop muted></video> -->
        <!-- <video class="thread3" ref="twohundwh" src="https://edgistify.s3.ap-south-1.amazonaws.com/media/website2023_video/twohundwh.mp4" type="video/mp4" loop -->
        <!-- muted></video>
        <video class="thread4" ref="allmetro" src="https://edgistify.s3.ap-south-1.amazonaws.com/media/website2023_video/allmetro.mp4" type="video/mp4" loop
          muted></video> -->
        <!-- <v-img src="/Homepage/OurPresence/map.png" contain></v-img> -->
      </v-col>
      <v-col class="options-container" md="6">
        <v-col class="option py-0">
          <span data-aos="fade-up" data-aos-once="true" data-aos-easing="ease-in" data-aos-duration="1000"
            v-on:mouseenter="playVideo('thread1', 0)" v-on:mouseleave="stopVideo('thread1')"
            :class="getLinkClasses(0)">50+ Cities</span>
        </v-col>
        <v-col class="option py-0">
          <span data-aos="fade-up" data-aos-once="true" data-aos-easing="ease-in" data-aos-duration="1000"
            v-on:mouseenter="playVideo('thread3', 1)" v-on:mouseleave="stopVideo('thread3')"
            :class="getLinkClasses(1)">100+ Warehouses</span>
        </v-col>
        <v-col class="option py-0">
          <span data-aos="fade-up" data-aos-once="true" data-aos-easing="ease-in" data-aos-duration="1100"
            v-on:mouseenter="playVideo('thread4', 2)" v-on:mouseleave="stopVideo('thread4')"
            :class="getLinkClasses(2)">4.5 Lac Sqft Managed Space</span>
        </v-col>
        <v-col class="option py-0">
          <span data-aos="fade-up" data-aos-once="true" data-aos-easing="ease-in" data-aos-duration="1200"
            v-on:mouseenter="playVideo('thread2', 3)" v-on:mouseleave="stopVideo('thread2')"
            :class="getLinkClasses(3)">Pan India Delivery</span>
        </v-col>
      </v-col>
    </v-row>
  </v-container>
</template>

<style lang="scss" scoped>
.our-presence-container {
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 50.625rem;
  background-color: #0c0c0c;
  padding: 0 6%;

  // background-image: url("/Homepage/OurPresence/grid-top.png");
  // background-position: top;
  // background-size: contain;
  .heading-container {
    display: flex;
    width: 100%;
    height: 20%;
    align-items: center;

    h2 {
      font-size: 42px;
      font-family: "Noto Serif";
      line-height: 58px;
      color: white !important;
    }
  }

  .content-container {
    .map-container {
      transition: all 1s ease-in-out;

      .thread1,
      .thread2,
      .thread3,
      .thread4 {
        position: absolute;
      }

      .thread2,
      .thread3,
      .thread4 {
        z-index: -1;
      }
    }

    .options-container {
      display: flex;
      flex-direction: column;
      align-items: center;
      width: 50%;
      height: 90%;

      :last-child {
        border-bottom: 1px solid #8d8d8d;
      }

      .option {
        display: flex;
        align-items: center;
        width: 50%;
        height: 25%;
        border-top: 1px solid #8d8d8d;
        // padding-left: 25px;

        :last-child {
          border-bottom: none;
        }

        span {
          color: #9c9c9c;
          font-size: 24px;
          font-family: "Outfit" !important;
        }

        .active-link {
          color: #fff;
        }
      }
    }
  }
}

@media (max-width: 850px) {
  .our-presence-container {
    display: flex;
    flex-direction: column;
    width: 100%;
    height: 20rem !important;
    background-color: #0c0c0c;
    padding: 4% 6% !important;

    .heading-container {
      // display: flex;
      // width: 100%;
      // padding: 0 2.75rem 0 2.75rem !important;
      height: auto !important;
      // align-items: center;

      h2 {
        font-weight: 500 !important;
        font-size: 1.5rem !important;
        line-height: 2rem !important;
        color: #fff !important;
      }
    }

    .content-container {
      // display: flex;
      // width: 100%;
      height: auto !important;
      // padding: 0 3.5rem 0 3.5rem !important;
      align-items: flex-start !important;
      justify-content: flex-end !important;
      padding: 10% 0 0 0 !important;

      .map-container {
        display: flex;
        align-items: unset !important;
        justify-content: center !important;
        width: 50%;
        height: 70%;
        padding: 0px !important;
        transition: all 1s ease-in-out;
        position: relative !important;

        .thread1,
        .thread2,
        .thread3,
        .thread4 {
          width: 166.77px !important;
          height: 185px !important;
        }

        .thread2,
        .thread3,
        .thread4 {
          z-index: -1;
        }

        video {
          position: absolute !important;
          left: 20% !important;
          top: 0% !important;
        }
      }

      .options-container {
        align-items: flex-end !important;
        justify-content: flex-start !important;
        // padding-top: 1rem !important;
        // width: 100% !important;
        // height: 100% !important;

        .option {
          width: 70% !important;
          height: 17% !important;
          padding-left: 0px !important;

          span {
            font-weight: 400 !important;
            font-size: 8.83448px !important;
            line-height: 11px !important;
          }
        }
      }
    }
  }
}
</style>

<script>
import aosMixin from "~/mixins/aos";

export default {

  data () {
    return {
      isSelected: true,
      activeLink: 0
    }
  },
  methods: {
    playVideo (videoName, index) {
      console.log(videoName, this.$el.getElementsByClassName(videoName));
      const imgEl = document.querySelector(`.${videoName}`);

      imgEl.style.zIndex = "2";
      this.activeLink = index
      //this.$refs[videoName].play();
      //this.$refs[videoName].style.zIndex = "2";
    },
    stopVideo (videoName) {
      console.log(videoName, this.$el.getElementsByClassName(videoName));

      //console.log(this.$refs[videoName]);
      // this.$refs[videoName].pause();
      // this.$refs[videoName].style.zIndex = "0";

      const imgEl = document.querySelector(`.${videoName}`);

      imgEl.style.zIndex = "0";
    },
    getLinkClasses (index) {
      return {
        'active-link': this.activeLink === index,
        'aos-animate': true,
        'aos-init': true,
      };
    },
  },
  mixins: [aosMixin],
};
</script>
