<template>
  <v-container fluid class="ouradvisor-container" id="our-advisors">
    <h1 class="title">Our Advisors</h1>
    <v-row class="ouradvisor-wrapper pa-0" no-gutters justify="space-between">
      <v-col sm="12" md="4" class="scm-wrapper-row1 px-md-6 pb-6" cols="12">
        <div class="img1-div">
          <v-img
            :src="`/Company/fung-strategic-investments-rajesh-ranavat-executive-director.jpg.jpg`"
            aspect-ratio="1"
            cover
            class="bg-grey-lighten-2"
          >
          </v-img>
          <h1>Rajesh Ranavat</h1>
          <p>Executive Director,</p>
          <p>Fung Strategic Holdings</p>
        </div>
      </v-col>

      <v-col sm="12" md="4" class="scm-wrapper-row1 px-md-6 pb-6" cols="12">
        <div class="img1-div">
          <v-img
            src="/Company/diageo-india-jitendra-mahajan.jpg.jpg"
            class="advisor-img"
          ></v-img>
          <h1>Jitendra Mahajan</h1>
          <p>Chief Supply Chain and Sustainability Officer,</p>
          <p>DIAGEO India</p>
        </div>
      </v-col>
      <v-col sm="12" md="4" class="scm-wrapper-row1 px-md-6 pb-6" cols="12">
        <div class="img1-div">
          <v-img
            src="/Company/adani-group-vikram-tandon-group-chro.jpg.jpg"
            class="advisor-img"
          ></v-img>
          <h1>Vikram Tandon</h1>
          <p>Group Chief Human Resources Officer,</p>
          <p>Adani Group</p>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup></script>

<style lang="scss" scoped>
.ouradvisor-container {
  width: 100%;
  background: black;
  padding: 0 6% 2% 6% !important;

  .scm-wrapper-row1:first-child {
    margin-left: -24px;
  }
  .scm-wrapper-row1:last-child {
    margin-right: -24px;
  }
  .ouradvisor-wrapper {
    h1 {
      font-family: "Outfit" !important;
      font-style: normal;
      font-weight: 500;
      font-size: 16px !important;
      line-height: 20px;
      padding-top: 12px;
      color: #ffffff;
      margin-bottom: 2px;
    }

    p {
      font-family: "Outfit";
      font-style: normal;
      font-weight: 300;
      font-size: 14px;
      line-height: 18px;
      margin-bottom: 2px;

      color: #ffffff;
    }
  }

  .title {
    font-family: "Noto Serif" !important;
    font-style: normal;
    font-weight: 500;
    font-size: 42px !important;
    line-height: 47px;
    color: #ffffff;
    padding-top: 36px;
    padding-bottom: 30px;

    line-height: 47px;
  }
}

@media screen and (max-width: 850px) {
  .ouradvisor-container {
    width: 100%;
    height: auto !important;
    background-image: none !important;
    padding: 0 30px !important;

    .scm-wrapper-row1:first-child {
      margin-left: 0;
    }
    .scm-wrapper-row1:last-child {
      margin-right: 0;
    }
    .img1-div {
      height: auto !important;
    }

    .ouradvisor-wrapper {
      height: 90% !important;
      margin: 0rem !important;
    }

    .col {
      padding-right: 0 !important;
      padding-bottom: 8px !important;
    }

    .title {
      font-size: 30px !important;
      line-height: 2.063rem !important;
    }
  }
}
</style>
