<template>
  <v-container fluid class="platform-offers-container pa-0">
    <v-row no-gutters class="main-wrapper">
      <v-col cols="12" class="heading-wrapper px-0">
        <h1>Our Platform Offers</h1>
      </v-col>
      <v-col cols="12" sm="12" md="12" class="offers-wrapper">
        <v-row
          no-gutters
          class="card-container px-0"
          justify="space-between"
          align="center"
        >
          <v-col cols="6" sm="6" md="3" class="pr-md-6 pr-3">
            <div class="card">
              <p>Vendor Management</p>
            </div>
          </v-col>
          <v-col cols="6" sm="6" md="3" class="px-md-6 pl-3">
            <div class="card">
              <p>PO Creation</p>
            </div>
          </v-col>
          <v-col cols="6" sm="6" md="3" class="px-md-6 pr-3">
            <div class="card">
              <p>GRN</p>
            </div>
          </v-col>
          <v-col cols="6" sm="6" md="3" class="pl-md-6 pl-3">
            <div class="card">
              <p>Quality Check</p>
            </div>
          </v-col>
        </v-row>
        <v-row
          no-gutters
          class="card-container px-0"
          justify="space-between"
          align="center"
        >
          <v-col cols="6" sm="6" md="3" class="pr-md-6 pr-3">
            <div class="card">
              <p>Put-away Process</p>
            </div>
          </v-col>
          <v-col cols="6" sm="6" md="3" class="px-md-6 pl-3">
            <div class="card">
              <p>Shelf Management</p>
            </div>
          </v-col>
          <v-col cols="6" sm="6" md="3" class="px-md-6 pr-3">
            <div class="card">
              <p>Stock Shelving</p>
            </div>
          </v-col>
          <v-col cols="6" sm="6" md="3" class="pl-md-6 pl-3">
            <div class="card">
              <p>Inventory Management</p>
            </div>
          </v-col>
        </v-row>
        <v-row
          no-gutters
          class="card-container px-0"
          justify="space-between"
          align="center"
        >
          <v-col cols="6" sm="6" md="3" class="pr-md-6 pr-3">
            <div class="card">
              <p>Barcode Generation</p>
            </div>
          </v-col>
          <v-col cols="6" sm="6" md="3" class="px-md-6 pl-3">
            <div class="card">
              <p>Auto Order Allocation</p>
            </div>
          </v-col>
          <v-col cols="6" sm="6" md="3" class="px-md-6 pr-3">
            <div class="card">
              <p>Auto Shipping Partner Assignment</p>
            </div>
          </v-col>
          <v-col cols="6" sm="6" md="3" class="pl-md-6 pl-3">
            <div class="card">
              <p>Auto Carrier Assignment</p>
            </div>
          </v-col>
        </v-row>
        <v-row
          no-gutters
          class="card-container px-0"
          justify="space-between"
          align="center"
        >
          <v-col cols="6" sm="6" md="3" class="pr-md-6 pr-3">
            <div class="card">
              <p>Order Picking</p>
            </div>
          </v-col>
          <v-col cols="6" sm="6" md="3" class="px-md-6 pl-3">
            <div class="card">
              <p>Packing</p>
            </div>
          </v-col>
          <v-col cols="6" sm="6" md="3" class="px-md-6 pr-3">
            <div class="card">
              <p>Packing</p>
            </div>
          </v-col>
          <v-col cols="6" sm="6" md="3" class="pl-md-6 pl-3">
            <div class="card">
              <p>Invoice and Label Printing</p>
            </div>
          </v-col>
        </v-row>
        <v-row
          no-gutters
          class="card-container px-0"
          justify="space-between"
          align="center"
        >
          <v-col cols="6" sm="6" md="3" class="pr-md-6 pr-3">
            <div class="card">
              <p>Manifest Generation</p>
            </div>
          </v-col>
          <v-col cols="6" sm="6" md="3" class="px-md-6 pl-3">
            <div class="card">
              <p>Dispatching</p>
            </div>
          </v-col>
          <v-col cols="6" sm="6" md="3" class="px-md-6 pr-3">
            <div class="card">
              <p>Shipping</p>
            </div>
          </v-col>
          <v-col cols="6" sm="6" md="3" class="pl-md-6 pl-3">
            <div class="card">
              <p>Kitting and Bundling</p>
            </div>
          </v-col>
        </v-row>
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
.platform-offers-container {
  height: 50rem;
  background: #ffffff;

  .main-wrapper {
    height: auto;
    padding: 4% 6%;

    .heading-wrapper {
      h1 {
        font-family: "Noto Serif";
        font-style: normal;
        font-weight: 400;
        font-size: 42px;
        line-height: 3.563rem;
        color: #0c0c0c;
      }
    }

    .offers-wrapper {
      height: auto;

      .card-container {
        display: flex;
        width: 100%;
        height: 35%;

        .card {
          height: 4.5rem;
          background: #f3f3f5;
          display: flex;
          justify-content: center;
          align-items: center;

          p {
            font-family: "Outfit";
            font-style: light;
            font-weight: 300;
            font-size: 14px;
            line-height: 20px;
            padding: 24px;
            margin: 0;
          }
        }
      }
    }
  }
}

@media screen and (max-width: 850px) {
  .platform-offers-container {
    height: auto !important;
    background: #ffffff !important;

    .main-wrapper {
      flex-direction: column !important;

      .heading-wrapper {
        h1 {
          font-family: "Noto Serif" !important;
          font-style: normal !important;
          font-weight: 400 !important;
          font-size: 30px !important;
          line-height: 2.5rem !important;
          color: #0c0c0c !important;
        }
      }

      .offers-wrapper {
        padding-top: 5% !important;
        flex-direction: row !important;

        .card-container {
          height: auto !important;

          .card {
            width: auto !important;
            height: 4rem !important;
            margin-bottom: 10% !important;
            text-align: center;

            p {
              font-family: "Outfit" !important;
              font-style: normal !important;
              font-weight: 400 !important;
              font-size: 0.5rem !important;
              line-height: 0.625rem !important;
              padding: 0 !important;
            }
          }
        }
      }
    }
  }
}
</style>
