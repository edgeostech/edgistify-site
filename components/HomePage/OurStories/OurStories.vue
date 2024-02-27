<template>
  <v-container fluid class="our-stories-container">
    <div class="heading-container">
      <h2
        data-aos="fade-up"
        data-aos-once="true"
        data-aos-easing="ease-in"
        data-aos-duration="800"
      >
        We are Proud of the Industry Recognition Received
      </h2>
    </div>
    <v-row no-gutters class="content-container py-4">
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
          <v-col class="source px-0 h1">Silicon India</v-col>
          <v-col class="news px-0 para">
            Edgistify’s SaaS based platform is holding the clean data for the
            industry in a scientific manner which brings speed and efficiency
            for all the stakeholders...
          </v-col>
          <nuxt-link
            :to="{ path: '/resources/access-the-tools-you-need-to-learn-resources-edgistify', hash: '#resource-media' }"
            style="text-decoration: none; color: inherit"
          >
            <v-col class="action px-0">Read more</v-col>
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
          <v-col class="source px-0 h1">ITL News</v-col>
          <v-col class="news px-0 para">
            Edgistify got selected as one of the top 11 startups from 600+
            applications to make it to cohort 2020, a scale-up program for
            growth-stage startups in India...
          </v-col>
          <nuxt-link
            :to="{ path: '/resources/access-the-tools-you-need-to-learn-resources-edgistify', hash: '#resource-media' }"
            style="text-decoration: none; color: inherit"
          >
            <v-col class="action px-0">Read more</v-col>
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
          <v-col class="source px-0 h1">ClickPost</v-col>
          <v-col class="news px-0 para">
            Clickposts lists Edgistify as one of the best 10 logistics startups
            in India for e-commerce companies that provides niche goods and
            services...
          </v-col>
          <nuxt-link
            :to="{ path: '/resources/access-the-tools-you-need-to-learn-resources-edgistify', hash: '#resource-media' }"
            style="text-decoration: none; color: inherit"
          >
            <v-col class="action px-0">Read more</v-col>
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
          <v-col class="source px-0 h1">Logistic Insider</v-col>
          <v-col class="news px-0 para">
            Logistics insider identifies Edgistify as one of the top 10
            promising logistics companies in 2021. It highlights intent to
            become India’s leading logistics..
          </v-col>
          <nuxt-link
            :to="{ path: '/resources/access-the-tools-you-need-to-learn-resources-edgistify', hash: '#resource-media' }"
            style="text-decoration: none; color: inherit"
          >
            <v-col class="action px-0">Read more</v-col>
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
    // padding: 30px 20px !important;
  }

  .heading-container h2 {
    font-size: 24px !important;
    line-height: 30px;

  }

  .content-container {
    flex-wrap: wrap !important;
    display: flex !important;
    justify-content: space-between;

    .last-card:last-child {
      border-right: none !important;
    }

    // padding-top: 20px;
    // padding-bottom: 20px;

    .main-card {
      display: flex !important;
    }

    .content {
      // flex: 1 0 33.33%;
      margin: 6% 0 !important;
      // display: flex;
      align-items: flex-start !important;
      border-left: 0.5px solid #8d8d8d !important;

      color: #1e1e1e !important;

      .action {
        color: #00a699;
      }

      // justify-content: center;

      .source {
        font-weight: 300 !important;
        font-size: 14px !important;
        line-height: 20px !important;
        letter-spacing: 0.015em !important;
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
        font-weight: 300 !important;
        font-size: 0.75rem !important;
        line-height: 10px !important;
        letter-spacing: 0.015em !important;
        font-family: "Outfit";
      }
    }

    .content:nth-child(2) {
      border-right: 0.5px solid #8d8d8d !important;
    }
  }
}

.our-stories-container {
  background-color: #fff;
  color: #1e1e1e;
  padding: 3% 6%;

  .heading-container {
    // display: flex;
    // width: 100%;
    height: auto;
    // align-items: center;

    h2 {
      font-size: 42px;
      font-family: "Noto Serif";
    }
  }

  .content-container {
    // display: flex;
    // width: 100%;
    height: auto;

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
      padding: 0 3%;
      border-left: 1px solid #8d8d8d;

      :last-child {
        border: none;
      }

      .source {
        font-family: "Noto Serif";
        font-size: 1rem;
        line-height: 20px;
        margin-bottom: 20px;
      }

      .news {
        font-size: 1rem;
        line-height: 20px;
        margin-bottom: 20px;
        font-weight: 300;
      }

      .action {
        font-size: 1rem;
        line-height: 20px;
        margin-bottom: 20px;
        font-weight: 300;
        font-family: "Outfit";
      }

      &:hover {
        color: #1e1e1e;

        .action {
          color: #00a699;
        }
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
