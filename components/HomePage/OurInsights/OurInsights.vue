<template>
  <v-container fluid class="our-stories-container pa-0">
    <v-col class="heading-container">
      <h2
        data-aos="fade-up"
        data-aos-once="true"
        data-aos-easing="ease-in"
        data-aos-duration="800"
      >
        Featured Insights
      </h2>
    </v-col>
    <v-row no-gutters class="content-container pb-12">
      <v-col cols="12" sm="12" md="6" class="main-card">
        <v-col
          cols="6"
          sm="6"
          md="6"
          class="content"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="900"
        >
          <v-col class="source pa-0 para">Case Studies</v-col>
          <v-col class="px-0">
            <div class="image-container1"></div>
          </v-col>
          <v-col class="news px-0 para">
            Bisleri International is an Indian company that is best known for
            its eponymous brand of bottled water.
          </v-col>

          <nuxt-link
            :to="{ path: '/resources/access-the-tools-you-need-to-learn-resources-edgistify', hash: '#resource-Case-studies' }"
            style="text-decoration: none; color: inherit"
          >
            <v-col class="action pa-0">Read more</v-col>
          </nuxt-link>
        </v-col>
        <v-col
          cols="6"
          sm="6"
          md="6"
          class="content"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="1000"
        >
          <v-col class="source pa-0 para">Blog</v-col>
          <v-col class="px-0">
            <div class="image-container2"></div>
          </v-col>
          <v-col class="news px-0 para">
            Data Analytics in logistics is transforming from a “nice-to-have”
            into a “must-have”.
          </v-col>
          <nuxt-link
            :to="{ path: '/resources/access-the-tools-you-need-to-learn-resources-edgistify', hash: '#resource-blog' }"
            style="text-decoration: none; color: inherit"
          >
            <v-col class="action pa-0">Read more</v-col>
          </nuxt-link>
        </v-col>
      </v-col>
      <v-col cols="12" sm="12" md="6" class="main-card">
        <v-col
          cols="6"
          sm="6"
          md="6"
          class="content"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="1100"
        >
          <v-col class="source pa-0 para">Media</v-col>
          <v-col class="px-0">
            <div class="image-container3"></div>
          </v-col>
          <v-col class="news px-0 para">
            Edgistify partners with Eunimart to enter into hyper-local delivery
            pan India.
          </v-col>
          <nuxt-link
            :to="{ path: '/resources/access-the-tools-you-need-to-learn-resources-edgistify', hash: '#resource-media' }"
            style="text-decoration: none; color: inherit"
          >
            <v-col class="action pa-0">Read more</v-col>
          </nuxt-link>
        </v-col>
        <v-col
          cols="6"
          sm="6"
          md="6"
          class="content last-card"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="1200"
        >
          <v-col class="source pa-0 para">Video</v-col>
          <v-col class="px-0">
            <div class="image-container4"></div>
          </v-col>
          <v-col class="news px-0 para">
            Edgistify | Fresh Produce Logistics | Hyperlocal-Delivery |
            Warehousing and Fulfillment | PAN India
          </v-col>
          <nuxt-link
            :to="{ path: '/resources/access-the-tools-you-need-to-learn-resources-edgistify', hash: '#resource-Videos' }"
            style="text-decoration: none; color: inherit"
          >
            <v-col class="action pa-0">Read more</v-col>
          </nuxt-link>
        </v-col>
      </v-col>
    </v-row>
  </v-container>
</template>

<style lang="scss" scoped>
@media (max-width: 850px) {
  .our-stories-container {
    height: auto !important;
    // padding: 0 20px !important;

    .heading-container {
      h2 {
        font-size: 1.5rem !important;
      }
    }

    .heading-container {
      padding-top: 30px !important;
    }

    .content-container {
      display: flex !important;
      flex-wrap: wrap !important;
      padding-bottom: 20px !important;
      justify-content: space-between;

      .last-card:last-child {
        border-right: 1px solid #8d8d8d !important;
      }

      .main-card {
        display: flex !important;
      }

      .content {
        // flex: 1 0 18%;
        // margin: 5px;
        margin: 6% 0 !important;

        color: #1e1e1e !important;

        .action {
          color: #00a699;
        }

        display: flex;
        align-items: flex-start !important;
        justify-content: center;
        padding: 0 3% !important;

        .image-container1,
        .image-container2,
        .image-container3,
        .image-container4 {
          height: 4.569rem !important;
          background-size: cover !important;
        }

        .image-container1 {
          background-image: url("/Homepage/OurInsightes/insights-4-color.png") !important;
        }

        .image-container2 {
          background-image: url("/Homepage/OurInsightes/insights-1-color.png") !important;
        }

        .image-container3 {
          background-image: url("/Homepage/OurInsightes/insights-2-color.png") !important;
        }

        .image-container4 {
          background-image: url("/Homepage/OurInsightes/insights-3-color.png") !important;
        }
      }

      .source {
        font-family: "Noto Serif" !important;
        font-size: 14px !important;
        line-height: 20px !important;
        margin-bottom: 0 !important;
      }

      .news {
        font-weight: 300 !important;
        font-size: 10px !important;
        line-height: 14px !important;
        letter-spacing: 0.015em !important;
        margin-bottom: 0 !important;
      }

      .action {
        font-family: "Noto Serif" !important;
        font-size: 0.7rem !important;
        line-height: 20px !important;
        margin-bottom: 0 !important;
      }

      .content:nth-child(2) {
        border-right: 1px solid #8d8d8d;
      }
    }
  }
}

.our-stories-container {
  // padding: 0 94px;
  background-color: #fff;
  color: #1e1e1e;

  .heading-container {
    display: flex;
    width: 100%;
    height: auto;
    align-items: center;
    padding: 2% 6%;

    h2 {
      font-size: 42px;
      font-family: "Noto Serif";
    }
  }

  .content-container {
    display: flex;
    width: 100%;
    height: auto;
    padding: 0% 6%;

    .last-card:last-child {
      border-right: 1px solid #8d8d8d;
    }

    .main-card {
      display: flex;
    }

    .content {
      display: flex;
      flex-direction: column;
      height: fit-content;
      color: #8d8d8d;
      padding: 0 30px;
      border-left: 1px solid #8d8d8d;

      :last-child {
        border: none;
      }

      .source {
        font-family: "Noto Serif";
        font-size: 1rem;
        line-height: 20px;
      }

      .image-container1 {
        display: flex;
        height: 11.25rem;
        background-image: url("/Homepage/OurInsightes/insights-4.png");
        background-size: auto;
        transition: 0.2s all ease-in-out;
      }

      .image-container2 {
        display: flex;
        height: 11.25rem;
        background-image: url("/Homepage/OurInsightes/insights-1.png");
        background-size: auto;
        transition: 0.2s all ease-in-out;
      }

      .image-container3 {
        display: flex;
        height: 11.25rem;
        background-image: url("/Homepage/OurInsightes/insights-2.png");
        background-size: auto;
        transition: 0.2s all ease-in-out;
      }

      .image-container4 {
        display: flex;
        height: 11.25rem;
        background-image: url("/Homepage/OurInsightes/insights-3.png");
        background-size: auto;
        transition: 0.2s all ease-in-out;
      }

      .news {
        font-size: 16px;
        line-height: 20px;
        font-weight: 300;
      }

      .action {
        font-size: 16px;
        line-height: 20px;
        font-weight: 300;
        align-items: flex-start;
        font-family: "Outfit";
      }

      &:hover {
        color: #1e1e1e;

        .action {
          color: #00a699;
        }

        .image-container1 {
          background-image: url("/Homepage/OurInsightes/insights-4-color.png");
        }

        .image-container2 {
          background-image: url("/Homepage/OurInsightes/insights-1-color.png");
        }

        .image-container3 {
          background-image: url("/Homepage/OurInsightes/insights-2-color.png");
        }

        .image-container4 {
          background-image: url("/Homepage/OurInsightes/insights-3-color.png");
        }
      }
    }
  }

  .overlap-container {
    position: absolute;
    z-index: 2;
    display: flex;
    width: 100%;
    height: 116px;
    background-color: #fff;
    margin-top: 360px;
    color: #00a699;

    .text {
      display: flex;
      flex-direction: column;
      width: 70%;
      height: 100%;
      padding: 0 30px;

      .head {
        display: flex;
        width: 100%;
        height: 65%;
        align-items: flex-end;

        h2 {
          font-weight: 600;
          font-size: 48px;
          line-height: 60px;
        }
      }

      .sub-head {
        display: flex;
        width: 100%;
        height: 35%;
        margin-top: -15px;

        span {
          font-size: 12px;
        }
      }
    }

    .action {
      display: flex;
      width: 30%;
      height: 100%;
      align-items: center;
      justify-content: center;
      font-family: "Outfit";

      span {
        display: flex;
        width: 167px;
        height: 42px;
        align-items: center;
        justify-content: center;

        background: #00a699;
        border: 1px solid #00a699;
        border-radius: 50px;
        color: #fff;

        font-family: "Noto Serif";
        font-style: normal;
        font-weight: 600;
        font-size: 16px;
        line-height: 22px;
      }
    }
  }
}
</style>
<script>
import aosMixin from "~/mixins/aos";

export default {
  mixins: [aosMixin],
};
</script>
