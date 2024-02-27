<template>
  <v-container fluid class="company-ourjourney" id="our-journey">
    <h1>Our Journey</h1>
    <v-row class="ourjourney-wrapper" no-gutters>
      <v-col sm="12" md="6" class="pr-6 pb-6 left-content">
        <div class="banner-left">
          <p>
            In 2017, three friends from IIT and NIT founded Edgistify with a
            clear mission to address the growing need for efficient, structured,
            and digitally-controlled supply chains in India's rapidly expanding
            manufacturing sector.
          </p>

          <p>
            At Edgistify, we initially focused on building a warehouse discovery
            platform that rated and benchmarked over 200 key parameters for
            warehouses. Over the next three years, we created a database of
            50,000+ warehouses to simplify and make the process of warehouse
            procurement transparent through a digital platform.
          </p>

          <p>
            In 2021, we pivoted to handling full-stack warehousing operations
            across a network of over 200 dark stores and warehouses in metro and
            tier 2-3 cities across India, expanding our operational capabilities
            and setting the stage for our next phase of growth.
          </p>
          <p>
            As we scaled our operations, we recognized the need for an
            integrated supply chain that would enable us to combine cutting-edge
            technology with industry best practices. That led to the development
            of EdgeOS, an in-house software that allows us to design, build, and
            run highly efficient and customized supply chains for B2B and B2C
            businesses.
          </p>
          <p style="padding-bottom: 2rem">
            Today, Edgistify is a leading player in the Indian logistics
            industry, trusted by businesses of all sizes to provide world-class
            supply chain solutions. We are committed to continuous innovation,
            leveraging the latest technologies and best practices to deliver
            maximum value to our clients and help them stay ahead of the
            competition.
          </p>
          <nuxt-link
            :to="{ path: '/careers/exciting-opportunities-join-the-team-edgistify', hash: '#careers-joinus' }"
            class="join-is-btn"
            style="text-decoration: none; color: inherit; margin-top: 16px"
            @click.native="scrollToLocation"
          >
            <span class="btn bg-white">Join Us</span>
          </nuxt-link>
        </div>
      </v-col>
      <v-col sm="12" md="6" class="pl-md-6 pb-6">
        <v-img
          src="/Company/edgistify-journey-timeline.jpg.png"
          style="height: 100%"
          class="right-img"
          alt="Edgistify's journey timeline showcasing their growth and success in the supply chain industry"
        ></v-img>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
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
};
</script>

<style lang="scss" scoped>
.btn {
  padding: 11.5px 26px;
  font-family: "Noto Serif";
  gap: 10px;
  height: 48px;
  background: #00a699;
  border-radius: 38px;
  color: white;
  margin-top: 12px;
}

.company-ourjourney {
  padding: 2% 6%;

  .left-content {
    position: relative;
  }
  .join-is-btn {
    position: absolute;
    bottom: 32px;
  }
  h1 {
    color: #161616;
    font-size: 35px;
    line-height: 42px;
    font-family: "Noto Serif";
    font-style: normal;
    font-weight: 500;
    margin-bottom: 1.25rem;
  }

  .ourjourney-wrapper {
    background-color: #ffff;

    .banner-left {
      p {
        color: #5f5f5f;
        font-family: "Outfit";
        font-style: normal;
        font-weight: lighter;
        font-size: 16px;
        line-height: 20px;
        margin-bottom: 0.85rem;
      }
    }
  }
}

@media screen and (max-width: 850px) {
  .join-is-btn {
    display: flex;
    justify-content: center;
    margin-top: 0 !important;
    position: unset !important;
  }
  .company-ourjourney {
    height: auto !important;
    width: 100%;
    padding: 6%;

    h1 {
      font-size: 30px !important;
    }
    .ourjourney-wrapper {
      width: 100%;
      display: flex;
      height: auto !important;
      justify-content: center;
      align-items: center;
      background-color: #ffff;
      flex-direction: column-reverse;

      .col {
        padding-right: 0 !important;
      }

      .banner-left {
        width: 100% !important;
        margin: 0 !important;
        justify-content: flex-start;

        h1 {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 300;
          font-size: 24px;
          line-height: 33px;
          color: #161616;
        }

        p {
          color: #5f5f5f;
          font-family: "Outfit";
          font-style: normal;
          font-weight: lighter;
          font-size: 16px !important;
          line-height: 20px !important;
        }
      }
    }
  }
}
</style>
