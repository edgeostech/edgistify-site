<template>
  <v-container fluid class="resource-media" id="resource-media">
    <h1 class="page-title">Media Presence</h1>

    <v-row no-gutters class="resource-wrapper">
      <v-col cols="6" sm="6" md="3" class="pr-6">
        <div class="specialists-details">
          <a
            href="https://www.itln.in/supply-chain-labs-announces-11-startups-for-cohort-2020"
            target="_blank"
          >
            <v-img src="/Resource/first.png" class="img"></v-img>
          </a>
          <div class="info-text">
            <h1>
              Supply Chain Labs by Lumis 
              - Cohort 2020
            </h1>
            <p>-ITL News</p>
          </div>
        </div>
      </v-col>
      <v-col  cols="6" sm="6" md="3" class="px-6">
        <div class="specialists-details">
          <a
            href="https://www.marketinginasia.com/indias-top-10-supply-chain-and-logistics-startups/"
            target="_blank"
          >
            <v-img src="/Resource/second.png" class="img"></v-img>
          </a>
          <div class="info-text">
            <h1>
              India's Top 10 Supply Chain and logistics
              Startups
            </h1>
            <p>-Marketing In Asia</p>
          </div>
        </div>
      </v-col>
      <v-col cols="6" sm="6" md="3" class="px-6">
        <div class="specialists-details">
          <a
            href="https://www.openpr.com/news/2351932/india-last-mile-delivery-market-top-key-players-delhivery-e"
            target="_blank"
          >
          <v-img src="/Resource/third.png" class="img"></v-img>
          </a>
          <div class="info-text">
            <h1>
              Edgistify gets listed as one of India's Last
              Mile Delivery Market Top Key Players
            </h1>
            <p>-OpenPR</p>
          </div>
        </div>
      </v-col>
      <v-col cols="6" sm="6" md="3" class="pl-6">
        <div class="specialists-details">
          <a
            href="https://startup.siliconindia.com/vendor/edgistify-a-single-point-solution-for-all-logistics-needs-cid-4762.html"
            target="_blank"
          >
            <v-img src="/Resource/four.png" class="img"></v-img>
          </a>
          <div class="info-text">
            <h1>
              Edgistify: A single-point solution for all 
              logistics needs. Siliconindia- Startup City
            </h1>
            <p>-Silicon India</p>
          </div>
        </div></v-col
      >
    </v-row>
    <v-row no-gutters class="resource-wrapper mt-12">
      <v-col cols="6" sm="6" md="3" class="pr-6">
        <div class="specialists-details">
          <a
            href="https://www.logisticsinsider.in/top-10-logistics-startups-in-india/"
            target="_blank"
          >
            <v-img src="/Resource/five.png" class="img"></v-img>
          </a>
          <div class="info-text">
            <h1>
              Logistics insider identifies Edgistify as
              one of the top 10 promising logistics
              companies in 2021
            </h1>
            <p>-Logistics Insider</p>
          </div>
        </div>
      </v-col>
      <v-col cols="6" sm="6" md="3" class="px-6">
        <div class="specialists-details">
          <a
            href="https://www.itln.in/supply-chain-labs-announces-11-startups-for-cohort-2020"
            target="_blank"
          >
            <v-img src="/Resource/six.png" class="img"></v-img>
          </a>
          <div class="info-text">
            <h1>
              Edgistify got listed as one of the top 11
              startups from 600+ applications to
              make it to cohort 2020
            </h1>
            <p>-ITL News</p>
          </div>
        </div></v-col
      >
      <v-col cols="6" sm="6" md="3" class="px-6"
        ><div class="specialists-details">
          <a
            href="https://www.clickpost.ai/blog/top-10-ecommerce-logistics-startups-in-india"
            target="_blank"
          >
          <v-img src="/Resource/seven.png" class="img"></v-img>
          </a>
          <div class="info-text">
            <h1>
              Clickposts lists Edgistify as one of the
              best 10 logistics startups in India for
              e-commerce companies
            </h1>
            <p>-Clickpost</p>
          </div>
        </div>
      </v-col>
      <v-col cols="6" sm="6" md="3" class="pl-6">
        <div class="specialists-details">
          <a
            href="https://theprint.in/ani-press-releases/edgistify-partners-with-eunimart-to-enter-into-hyper-local-delivery-pan-india/931625/"
            target="_blank"
          >
            <v-img src="/Resource/eight.png" class="img"></v-img>
          </a>
          <div class="info-text">
            <h1 class="print-header">
              Edgistify partners with Eunimart to
              enter into hyper-local delivery PAN India
            </h1>
            <p>-The Print</p>
          </div>
        </div></v-col
      >
    </v-row>
  </v-container>
</template>
<script setup></script>

<style lang="scss" scoped>
@media (max-width: 850px) {

  .resource-media {
  padding: 0 6%;
  h1.page-title {
    font-family: "Noto Serif";
    font-style: normal;
    font-weight: 300;
    font-size: 30px !important;
    line-height: 63px;
    color: #0c0c0c;
    margin: 2% 0 2%;
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

  .specialists-details {
      .img {
        height: 200px !important;
      }
    }
  .row {
      margin-top: 0 !important;
    }
}
.resource-media {
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
    .margin-top {
      margin-top: 40px;
    }

    .specialists-details {
      .img {
        height: 278px;
      }

      .info-text {
        width: 100%;
        margin: 12px 0;

        h1 {
          font-family: "Outfit";
          font-style: normal;
          height: fit-content;
          font-weight: 300;
          font-size: 15px;
          line-height: 20px;
          margin-bottom: 10px;
          color: #313131;
        }

        .print-header {
          margin-bottom: 28px !important;
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
