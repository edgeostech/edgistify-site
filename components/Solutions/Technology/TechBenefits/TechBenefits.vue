<template>
  <v-container fluid class="tech-benefits-main">
    <v-row no-gutters class="cards-container">
      <v-col cols="6" sm="6" md="3" class="pr-3 pb-6 pr-md-6 pb-md-6">
        <div class="card">
          <div class="icon-container mrktplace-shipping-partner"></div>
          <div class="title">
            Pre-Integrated Marketplaces <br />
            and Shipping Partner
          </div>
        </div>
      </v-col>
      <v-col cols="6" sm="6" md="3" class="pl-3 pb-6 px-md-6 pb-md-6">
        <div class="card ">
          <div class="icon-container improved-visibility-accuracy"></div>
          <div class="title">
            Improved Inventory Visibility <br />
            and accuracy
          </div>
        </div>
      </v-col>
      <v-col cols="6" sm="6" md="3" class="pr-3 pb-6 px-md-6 pb-md-6">
        <div class="card ">
          <div class="icon-container quick-dispatch"></div>
          <div class="title">
            Quick <br />
            Dispatch
          </div>
        </div>
      </v-col>
      <v-col cols="6" sm="6" md="3" class="pl-3 pb-6 pl-md-6 pb-md-6">
        <div class="card ">
          <div class="icon-container minimal-manpower"></div>
          <div class="title">
            Minimal <br />
            Manpower
          </div>
        </div>
      </v-col>
      <v-col cols="6" sm="6" md="3" class="pr-3 pb-6 pr-md-6 py-md-6">
        <div class="card ">
          <div class="icon-container inward-outward-operations"></div>
          <div class="title">
            Effortless Inward and <br />
            Outward Operations
          </div>
        </div>
      </v-col>
      <v-col cols="6" sm="6" md="3" class="pl-3 pb-6 px-md-6 py-md-6">
        <div class="card ">
          <div class="icon-container picking-bundling"></div>
          <div class="title">
            FIFO FEFO-Based Picking <br />
            and Bundling
          </div>
        </div>
      </v-col>
      <v-col cols="6" sm="6" md="3" class="pr-3 pb-md-6 px-md-6 py-md-6">
        <div class="card ">
          <div class="icon-container return-exchange"></div>
          <div class="title">
            Returns and Exchange <br />
            Management
          </div>
        </div>
      </v-col>
      <v-col cols="6" sm="6" md="3" class="pl-3 pb-md-6 pl-md-6 py-md-6">
        <div class="card ">
          <div class="icon-container storage-work"></div>
          <div class="title">
            Strategic Storage <br />
            Network
          </div>
        </div>
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
.tech-benefits-main {
  height: auto;
  background: #fdfdfd;
  padding: 6%;

  .cards-container {
    height: auto;

    .card {
      height: 12.5rem;
      background: #F3F3F5;


    
      .icon-container {
        width: 100%;
        height: 50%;
        background-size: 15%;
        background-position: center;

        &.mrktplace-shipping-partner {
          background-image: url("/Solutions/technology/mrktplace-shipping-partner.png");
        }

        &.improved-visibility-accuracy {
          background-image: url("/Solutions/technology/improved-visibility-accuracy.png");
        }

        &.quick-dispatch {
          background-image: url("/Solutions/technology/quick-dispatch.png");
        }

        &.minimal-manpower {
          background-image: url("/Solutions/technology/minimal-manpower.png");
        }

        &.inward-outward-operations {
          background-image: url("/Solutions/technology/inward-outward-operations.png");
        }

        &.picking-bundling {
          background-image: url("/Solutions/technology/picking-bundling.png");
        }

        &.return-exchange {
          background-image: url("/Solutions/technology/return-exchange.png");
        }

        &.storage-work {
          background-image: url("/Solutions/technology/storage-work.png");
        }
      }

      .title {
        display: flex;
        text-align: center;
        align-items: center;
        justify-content: center;
        width: 100%;
        height: 30%;
        font-weight: 500;
        font-size: 1rem !important;
        color: #000000;
        font-family: 'Outfit' !important;
      }
    }
  }
}

@media (max-width: 850px) {
  .tech-benefits-main {
    .cards-container {
      .card {
        height: 8rem !important;

        .icon-container {
          height: 50% !important;
          background-size: 15% !important;
        }

        .title {
          font-size: 0.75rem !important;
          height: auto !important;
          line-height: 1rem !important;
        }
      }
    }
  }
}
</style>
