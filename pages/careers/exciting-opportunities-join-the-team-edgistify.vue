<template>
  <v-container fluid class="company-container" id="careers-container">
    <v-row class="mb-6 company-banner" no-gutters>
      <v-col sm="12" md="6">
        <div class="banner-left">
          <h1>
            Build a Flourishing Career in Supply Chain. <br />
            Join Us!
          </h1>
          <nuxt-link
            :to="{ path: '/careers/exciting-opportunities-join-the-team-edgistify', hash: '#careers-openposition' }"
            style="text-decoration: none; color: inherit"
            @click.native="scrollToLocation"
          >
            <span class="bg-white btn">View Job Openings</span>
          </nuxt-link>
        </div>
      </v-col>
      <v-col sm="12" md="6">
        <v-img
          src="/career/edgistify-team.gif.gif"
          alt="Edgistify Business professionals discussing strategies for better productivity in the office"
          cover
          class="bg-grey-lighten-2 image-gif"
        ></v-img>
      </v-col>
    </v-row>
    <whyJoinUs />
    <openPositions />
  </v-container>
</template>

<script>
import whyJoinUs from "../../components/Careers/whyJoinUs.vue";
import openPositions from "../../components/Careers/openPositions.vue";

export default {
  components: {
    whyJoinUs,
    openPositions,
  },
  setup() {},
  data() {
    return {
      clicked: false,
    };
  },

  mounted() {
    window.addEventListener("scroll", this.onScroll);
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.onScroll);
  },
  methods: {
    onScroll() {
      // Get the current scroll position
      const currentScrollPosition =
        window.pageYOffset || document.documentElement.scrollTop; // Because of momentum scrolling on mobiles, we shouldn't continue if it is less than zero
      if (currentScrollPosition < 0) {
        return;
      } // Here we determine whether we need to show or hide the navbar
      this.showNavbar = currentScrollPosition < this.lastScrollPosition; // Set the current scroll position as the last scroll position
      this.lastScrollPosition = currentScrollPosition;
      if (!this.showNavbar) {
        this.showDropdown = false;
      }
    },

    scrollToLocation() {
      if (this.$route.hash) {
        const anchor = document.querySelector(`${this.$route.hash}`);
        if (anchor) {
          window.scrollTo({
            top: anchor.getBoundingClientRect().top + window.pageYOffset,
          });
        }
      }
    },

    onclick() {
      this.clicked = !this.clicked;
    },
  },
  head() {
    return {
      title: "Exciting Opportunities Join The Team Edgistify"
    };
  }
};
</script>

<style lang="scss" scoped>


.company-container {
  display: flex;
  width: 100%;
  height: auto;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 0;
  padding-top: 92px !important;


  // overflow: hidden;
  .company-banner {
    width: 100%;
    display: flex;
    height: 550px;
    justify-content: center;
    align-items: center;
    background-color: #ffff;

    .banner-left {
      height: 100%;
      display: flex;
      margin: 0 12%;
      flex-direction: column;
      justify-content: center;

      h1 {
        font-family: "Noto Serif";
        font-style: normal;
        font-weight: 300;
        font-size: 46.6116px;
        line-height: 63px;
        color: #161616;
        margin-bottom: 50px;
      }

      .btn {
        padding: 11.5px 26px;
        font-family: "Noto Serif";
        gap: 10px;
        height: 48px;
        background: #00a699;
        border-radius: 38px;
        color: white;
      }
    }

    .banner-image {
      width: 100%;
      height: 550px;
      background-size: contain;
      background-color: #000;
    }
  }
}

@media (max-width: 850px) {
  .company-container {
    width: 100% !important;
    height: auto !important;
    padding-top: 0 !important;
    .company-banner {
      width: 100%;
      display: flex;
      height: auto !important;
      flex-direction: column-reverse !important;
      justify-content: center;
      align-items: center;
      background-color: #ffff;

      .banner-left {
        width: 100% !important;
        margin: 0 !important;
        border: 1px solid #f3f3f5;

        h1 {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 300;
          font-size: 2rem !important;
          line-height: 2rem !important;
          color: #161616;
          margin: 30px !important;
        }

        a {
          margin: 30px auto;
        }

        .btn {
          width: 11.5rem !important;
          height: 2.438rem !important;
          border-radius: 1.938rem !important;
        }
      }

      .banner-right {
        width: 100% !important;

        .banner-image {
          height: auto !important;
        }
      }
    }
  }
}
</style>
