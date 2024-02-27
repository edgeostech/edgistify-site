<template>
  <v-container fluid class="supportservices-benefits-main">
    <!-- <div > -->
    <h1 class="heading-container pb-6 pt-6 pt-md-0">Areas of Work</h1>
    <!-- </div> -->
    <v-row no-gutters class="careers-wrapper-row1" justify="space-evenly">
      <v-col
        cols="4"
        sm="4"
        md="4"
        class="specialists-details pr-3 pb-3 pr-md-6 pb-md-6"
      >
        <v-col class="card pa-5 pa-md-10">
          <v-img src="/Solutions/consulting/img-1.png" class="img"></v-img>
          <div class="info-text">
            <p>
              Supply Chain<br />
              Optimization
            </p>
          </div>
        </v-col>
      </v-col>
      <v-col
        cols="4"
        sm="4"
        md="4"
        class="specialists-details px-2 pb-3 px-md-6 pb-md-6"
      >
        <v-col class="card pa-5 pa-md-10">
          <v-img src="/Solutions/consulting/img-2.png" class="img"></v-img>
          <div class="info-text">
            <p>
              Gap<br />
              Analysis
            </p>
          </div>
        </v-col>
      </v-col>
      <v-col
        cols="4"
        sm="4"
        md="4"
        class="specialists-details pl-3 pb-3 pl-md-6 pb-md-6"
      >
        <v-col class="card pa-5 pa-md-10">
          <v-img src="/Solutions/consulting/img-3.png" class="img"></v-img>
          <div class="info-text">
            <p>
              Network Planning <br />
              and Management
            </p>
          </div>
        </v-col>
      </v-col>
      <v-col
        cols="4"
        sm="4"
        md="4"
        class="specialists-details pr-3 py-3 pr-md-6 py-md-6"
      >
        <v-col class="card pa-5 pa-md-10">
          <v-img src="/Solutions/consulting/img-8.png" class="img"></v-img>
          <div class="info-text">
            <p>
              Geographic<br />
              Planning
            </p>
          </div>
        </v-col>
      </v-col>
      <v-col
        cols="4"
        sm="4"
        md="4"
        class="specialists-details px-2 py-3 px-md-6 py-md-6"
      >
        <v-col class="card pa-5 pa-md-10">
          <v-img src="/Solutions/consulting/img-7.png" class="img"></v-img>
          <div class="info-text">
            <p>
              Resource Planning <br />
              and Implementation
            </p>
          </div>
        </v-col>
      </v-col>
      <v-col
        cols="4"
        sm="4"
        md="4"
        class="specialists-details pl-3 py-3 pl-md-6 py-md-6"
      >
        <v-col class="card pa-5 pa-md-10">
          <v-img src="/Solutions/consulting/img-4.png" class="img"></v-img>
          <div class="info-text">
            <p>
              Material Flow and Warehouse<br />
              Layout Design
            </p>
          </div>
        </v-col>
      </v-col>
      <v-col
        cols="4"
        sm="4"
        md="4"
        class="specialists-details pr-3 py-3 pr-md-6 py-md-6"
      >
        <v-col class="card pa-5 pa-md-10">
          <v-img src="/Solutions/consulting/img-9.png" class="img"></v-img>
          <div class="info-text">
            <p>
              Digital<br />
              Transformation
            </p>
          </div>
        </v-col>
      </v-col>
      <v-col
        cols="4"
        sm="4"
        md="4"
        class="specialists-details px-2 py-3 px-md-6 py-md-6"
      >
        <v-col class="card pa-5 pa-md-10">
          <v-img src="/Solutions/consulting/img-6.png" class="img"></v-img>
          <div class="info-text">
            <p>
              Project Management<br />
              and Implementation
            </p>
          </div>
        </v-col>
      </v-col>
      <v-col
        cols="4"
        sm="4"
        md="4"
        class="specialists-details pl-3 py-3 pl-md-6 py-md-6"
      >
        <v-col class="card pa-5 pa-md-10">
          <v-img src="/Solutions/consulting/img-5.png" class="img"></v-img>
          <div class="info-text">
            <p>
              Inventory Planning<br />
              and Management
            </p>
          </div>
        </v-col>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup></script>

<style lang="scss" scoped>
.supportservices-benefits-main {
  height: auto;
  background: #1e1e1e;
  padding: 2% 6%;

  .heading-container {
    font-family: "Noto Serif";
    font-style: normal;
    font-weight: 400;
    font-size: 42px;
    line-height: 3.563rem;
    color: #ffffff;
    padding-bottom: 2%;
  }

  .careers-wrapper-row1 {
    display: flex;

    .specialists-details {
      height: auto;

      .card {
        background: #ffffff;
        height: 100%;

        .img {
          width: 18%;
          margin: auto;
        }

        .info-text {
          height: auto;
          margin: 1.5rem 0 1.5rem 0;

          p {
            font-family: "Outfit";
            font-style: normal;
            font-weight: 400;
            font-size: 16px;
            line-height: 20px;
            text-align: center;
            color: #000000;
          }
        }
      }
    }
  }
}

@media screen and (max-width: 850px) {
  .supportservices-benefits-main {
    height: auto;

    .heading-container {
      font-family: "Noto Serif";
      font-style: normal;
      font-weight: 400;
      font-size: 30px !important;
      line-height: 2.5rem !important;
      color: #ffffff;
    }

    .careers-wrapper-row1 {
      .specialists-details {
        .card {
          background: #ffffff !important;

          .img {
            width: 40% !important;
          }

          .info-text {
            margin: 5% !important;

            p {
              font-family: "Outfit" !important;
              font-style: normal !important;
              font-weight: 400 !important;
              font-size: 0.5rem !important;
              line-height: 1rem !important;
              text-align: center !important;
              color: #0c0c0c !important;
            }
          }
        }
      }
    }
  }
}
</style>
