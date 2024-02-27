<template>
  <v-container fluid class="resource-video" id="resource-Videos">
    <h1 class="page-title">Videos</h1>

    <v-row no-gutters class="resource-wrapper">
      <v-col cols="6" sm="6" md="3" class="pr-6">
        <div class="specialists-details">
          <a href="https://www.youtube.com/watch?v=-s8hr1QH--A" target="_blank">
            <v-img src="/Resource/video1.png" class="img"></v-img>
            <v-img src="/Resource/img1.png" class="img-hover"></v-img>
          </a>

          <div class="info-text">
            <h1>
              Real-time inventory tracking | Edgistify Fulfillment Service |
              Dark Store Network
            </h1>
          </div>
        </div>
      </v-col>
      <v-col cols="6" sm="6" md="3" class="pr-6 pl-6">
        <div class="specialists-details">
          <a href="https://www.youtube.com/watch?v=LHIvR21eEMc" target="_blank">
            <v-img src="/Resource/video2.png" class="img"></v-img>
            <v-img src="/Resource/img2.png" class="img-hover"></v-img>
          </a>
          <div class="info-text">
            <h1>Edgistify | On-demand warehousing | PAN India</h1>
          </div>
        </div>
      </v-col>
      <v-col cols="6" sm="6" md="3" class="px-6">
        <div class="specialists-details">
          <a
            href="https://www.youtube.com/watch?v=1-R7kcJxzNM&t=4s"
            target="_blank"
          >
            <v-img src="/Resource/video3.png" class="img"></v-img>
            <v-img src="/Resource/img2.png" class="img-hover"></v-img>
          </a>
          <div class="info-text">
            <h1>Edgistify | D2C | Warehousing and Fulfillment</h1>
          </div>
        </div>
      </v-col>
      <v-col cols="6" sm="6" md="3" class="pl-6">
        <div class="specialists-details">
          <a href="https://www.youtube.com/watch?v=ReG3dvXrqY8" target="_blank">
            <v-img src="/Resource/video4.png" class="img"></v-img>
            <v-img src="/Resource/img3.png" class="img-hover"></v-img>
          </a>
          <div class="info-text">
            <h1>Edgistify- Fulfillment Simplified</h1>
          </div>
        </div>
      </v-col>
    </v-row>
    <v-row no-gutters class="resource-wrapper mt-12 mb-12">
      <v-col cols="6" sm="6" md="3" class="pr-6">
        <div class="specialists-details">
          <a href="https://www.youtube.com/watch?v=DoVwLAv-1oc" target="_blank">
            <v-img src="/Resource/video5.png" class="img"></v-img>
            <v-img src="/Resource/img4.png" class="img-hover"></v-img>
          </a>
          <div class="info-text">
            <h1>Edgistify End-to-End Order Fulfillment</h1>
          </div>
        </div>
      </v-col>
      <v-col cols="6" sm="6" md="3" class="pr-6 pl-6">
        <div class="specialists-details">
          <a href="https://www.youtube.com/watch?v=yyowE6zPtd8" target="_blank">
            <v-img src="/Resource/video6.png" class="img"></v-img>
            <v-img src="/Resource/img5.png" class="img-hover"></v-img>
          </a>
          <div class="info-text">
            <h1>Deliver faster with India's largest dark store network</h1>
          </div>
        </div>
      </v-col>
      <v-col cols="6" sm="6" md="3" class="pr-6 pl-6">
        <div class="specialists-details">
          <a href="https://www.youtube.com/watch?v=JNFcPZsDEII" target="_blank">
            <v-img src="/Resource/video7.png" class="img"></v-img>
            <v-img src="/Resource/img6.png" class="img-hover"></v-img>
          </a>

          <div class="info-text">
            <h1>
              Fulfilling Hyperlocal delivery through robust Dark Store network
              PAN India
            </h1>
          </div>
        </div>
      </v-col>
      <v-col cols="6" sm="6" md="3" class="pl-6">
        <div class="specialists-details">
          <a href="https://www.youtube.com/watch?v=JdNEpr4vMZo" target="_blank">
            <v-img src="/Resource/video8.png" class="img"></v-img>
            <v-img src="/Resource/img7.png" class="img-hover"></v-img>
          </a>

          <div class="info-text">
            <h1>Edgistify | Fresh Produce Logistics | Hyperlocal-Delivery</h1>
          </div>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>
<script setup></script>

<style lang="scss" scoped>
@media (max-width: 850px) {

  .resource-video {
  h1.page-title {
    font-size: 30px !important;
  }}
  .resource-wrapper {
    height: auto !important;
    align-items: flex-start !important;
    .col-6:nth-child(odd) {
      padding-right: 12px !important;
      padding-left: 0 !important;
      padding-bottom: 12px;
    }
    .col-6:nth-child(even) {
      padding-right: 0 !important;
      padding-left: 0 !important;

    }
    
  }
  .row {
      margin-top: 0 !important;
    }
}
.resource-video {
  background: #fff;
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
  .resource-wrapper {
    .specialists-details:hover {
      .img-hover {
        display: flex;
      }
      .img {
        display: none;
        height: 184px;
    margin-bottom: 1rem;

      }
    }
    .img-hover {
      display: none;
      height: 184px;
      margin-bottom: 1rem;
    }
    .specialists-details {


      .img {
        height: 184px;
        margin-bottom: 1rem;
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
          margin-bottom: 0.25rem;
        }

        p {
          font-family: "Noto Serif";
          font-style: italic;
          font-weight: 400;
          font-size: 14px;
          line-height: 19px;
          color: #0c0c0c;
        }
      }
    }
  }
}
</style>
