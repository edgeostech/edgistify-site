<template>
  <v-container fluid class="resource-study" id="resource-Case-studies">
    <h1 class="page-title">Case Studies</h1>

    <v-row no-gutters class="resource-wrapper">
      <v-col cols="12" sm="6" md="6" class="pr-6">
        <div class="specialists-details">
          <label>Apna Mart</label>
          <v-img src="/Resource/study1.png" class="img"></v-img>
          <div class="info-text">
            <h1>
              Apna Mart operates a multi-level retail distribution network with
              100+ stores in  Chhattisgarh and Jharkhand
            </h1>
            <nuxt-link
              to="#"
              style="text-decoration: none; color: inherit"
            >
              <p>Read More</p>
            </nuxt-link>
          </div>
        </div>
      </v-col>
      <v-col cols="12" sm="6" md="6" class="pl-6">
        <div class="specialists-details">
          <label>Solar Square</label>
          <v-img src="/Resource/study2.png" class="img"></v-img>
          <div class="info-text">
            <h1>
              Solar Square is one of the leading residential rooftop solar
              installation companies. It has penetrated not only in metros but
              also in tier 1 and tier 2 cities of India
            </h1>
            <nuxt-link
              to="#"
              style="text-decoration: none; color: inherit"
            >
              <p>Read More</p>
            </nuxt-link>
          </div>
        </div>
      </v-col>
    </v-row>
    <v-row no-gutters class="resource-wrapper">
      <v-col cols="12" sm="6" md="6" class="pr-6">
        <div class="specialists-details">
          <label>Bisleri</label>
          <v-img src="/Resource/study3.png" class="img"></v-img>
          <div class="info-text">
            <h1>
              Bisleri International is an Indian company that is best known for
              its eponymous brand of bottled water
            </h1>
            <nuxt-link
              to="#"
              style="text-decoration: none; color: inherit"
            >
              <p>Read More</p>
            </nuxt-link>
          </div>
        </div></v-col
      >
      <v-col cols="12" sm="6" md="6" class="pl-6">
        <div class="specialists-details">
          <label>Saveo</label>
          <v-img src="/Resource/study4.png" class="img"></v-img>
          <div class="info-text">
            <h1>
              Saveo is a B2B brand that buys medicines from wholesalers and
              delivers to retailers (Marketplace of medicine). They are majorly
              present in AP, Telangana and Karnata...
            </h1>
            <nuxt-link
              to="#"
              style="text-decoration: none; color: inherit"
            >
              <p>Read More</p>
            </nuxt-link>
          </div>
        </div></v-col
      >
    </v-row>
  </v-container>
</template>
<script setup></script>

<style lang="scss" scoped>
@media (max-width: 850px) {

  .resource-study {
  h1.page-title {
    font-size: 30px !important;
  }}
  .resource-study {
    height: auto !important;

    .col-12:nth-child(odd) {
      padding-right: 12px !important;
      padding-left: 0 !important;
      padding-bottom: 12px;
    }
    .col-12:nth-child(even) {
      padding-right: 0 !important;
      padding-left: 0 !important;
    }
    .specialists-details {


      .info-text h1 {
        white-space: pre-line;
        font-size: 12px !important;
      }
    }
  }
}

.resource-study {
  background: #f3f3f5;
  padding: 0 6%;
  h1.page-title {
    font-family: "Noto Serif";
    font-style: normal;
    font-weight: 300;
    font-size: 42px;
    line-height: 63px;
    color: #0c0c0c;
    margin: 2% 0 2%;
  }

  .row {
    label {
      font-family: "Noto Serif";
      font-style: normal;
      font-weight: 400;
      font-size: 24px;
      line-height: 33px;
      color: #1e1e1e;
      display: block;
      margin-bottom: 24px;
    }

    .specialists-details:hover {
      .img {
        filter: grayscale(0%);
        transition: all 1s ease-in-out;
      }

      .info-text p {
        color: #00a699;
      }
    }

    .specialists-details {
      .img {
        height: 404px;
        margin-bottom: 1rem;
        filter: grayscale(100%);
      }

      .info-text {
        width: 100%;

        h1 {
          font-family: "Outfit";
          font-style: normal;
          font-weight: 300;
          font-size: 16px;
          line-height: 20px;
          color: #313131;
          margin-bottom: 1rem;
        }

        p {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 400;
          font-size: 16px;
          line-height: 22px;
          color: #616161;
        }
      }
    }
  }
}
</style>
