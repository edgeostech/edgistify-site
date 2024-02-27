<template>
  <v-container fluid class="integrations-main pa-0">
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-row no-gutters class="main_content">
      <v-col class="main_left_content" sm="12" md="6">
        <v-col class="main_title px-0">
          <h1>Integrations</h1>
        </v-col>
        <v-col class="content-header px-0">
          <h1>Plug and Play integrations for Faster Fulfillment</h1>
        </v-col>
        <!-- Mobile Layout  -->
        <v-col class="main_right_image px-0" v-if="isSmallDevice">
          <v-img
            src="/Solutions/technology/ecommerce-marketplace-integration-platform.png"
            contain
          />
        </v-col>
        <!-- Mobile Layout end  -->

        <v-col class="content-para px-0">
          <p>
            Integrate 50+ Marketplaces and Shopping Carts, 20+ courier partners
            and multiple ERP, CRM and accounting software. Experience seamless
            business communications, data flow, and reduced operations
            turnaround time.
          </p>
        </v-col>
        <v-col class="content-button px-0">
          <v-btn class="button bg-black" @click="showModal = true"
            >Schedule a Call</v-btn
          >
        </v-col>
      </v-col>
      <v-col class="main_right_image px-0" sm="12" md="6" v-if="!isSmallDevice">
        <v-img
          src="/Solutions/technology/ecommerce-marketplace-integration-platform.png"
          contain
        />
      </v-col>
    </v-row>
    <v-row no-gutters class="int-wrapper">
      <v-row no-gutters class="automate-main" id="automate-wrapper">
        <!-- <v-col cols="12" class="main-title-container">
               <h1>
                  Automate and integrate your <br />
                  marketplaces, suppliers and <br />
                  ERP with EdgeOS
               </h1>
            </v-col> -->
        <v-col cols="12" sm="12" md="12" class="main-mkt-wbs">
          <v-col cols="12" sm="12" md="6" class="main-title px-0 pr-md-6">
            <h1>
              Marketplaces <br />
              and Webstore
            </h1>
            <p>
              Integrate all the marketplaces and manage multiple channel orders
              on a single platform. Save your time switching between
              applications. Get a unified view of your orders.
            </p>
          </v-col>
          <v-col
            cols="12"
            sm="12"
            md="6"
            class="mkt-wbs-logos pl-md-6 px-0"
            v-if="!isSmallDevice"
          >
            <v-row
              no-gutters
              class="logos-container-1 mb-6"
              justify="space-between"
            >
              <v-col cols="3" md="2" sm="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/marketplace-webstore/shopify.png"
                  class="img"
                  contain
                />
              </v-col>
              <v-col cols="3" md="2" sm="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/marketplace-webstore/woo-commerce.png"
                  class="img"
                  contain
                />
              </v-col>

              <v-col cols="3" md="2" sm="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/marketplace-webstore/amazon.png"
                  class="img"
                  contain
                />
              </v-col>
              <v-col cols="3" md="2" sm="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/marketplace-webstore/flipkart.png"
                  class="img"
                  contain
                />
              </v-col>
              <v-col cols="3" md="2" sm="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/marketplace-webstore/meesho.png"
                  class="img"
                  contain
                />
              </v-col>
            </v-row>
            <v-row
              no-gutters
              class="logos-container-2"
              justify="end"
              style="gap: 4%"
            >
              <v-col cols="3" md="2" sm="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/marketplace-webstore/cred.png"
                  class="img"
                  contain
                />
              </v-col>

              <v-col cols="3" md="2" sm="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/marketplace-webstore/nykaa.png"
                  class="img"
                  contain
                />
              </v-col>
              <v-col cols="3" md="2" sm="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/marketplace-webstore/nykaa-fashion.png"
                  class="img"
                  contain
                />
              </v-col>
              <v-col cols="3" md="2" sm="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/marketplace-webstore/myntra.png"
                  class="img"
                  contain
                />
              </v-col>
            </v-row>
          </v-col>
        </v-col>
        <!-- Mobile Layout  -->
        <v-col class="main-mkt-wbs" v-if="isSmallDevice">
          <v-col cols="12" class="mkt-wbs-logos">
            <v-row no-gutters class="logos-container-1">
              <v-col cols="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/marketplace-webstore/shopify.png"
                  class="img"
                  contain
                />
              </v-col>
              <v-col cols="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/marketplace-webstore/woo-commerce.png"
                  class="img"
                  contain
                />
              </v-col>

              <v-col cols="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/marketplace-webstore/amazon.png"
                  class="img"
                  contain
                />
              </v-col>
              <v-col cols="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/marketplace-webstore/flipkart.png"
                  class="img"
                  contain
                />
              </v-col>
              <v-col cols="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/marketplace-webstore/meesho.png"
                  class="img"
                  contain
                />
              </v-col>
              <v-col cols="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/marketplace-webstore/cred.png"
                  class="img"
                  contain
                />
              </v-col>

              <v-col cols="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/marketplace-webstore/nykaa.png"
                  class="img"
                  contain
                />
              </v-col>
              <v-col cols="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/marketplace-webstore/nykaa-fashion.png"
                  class="img"
                  contain
                />
              </v-col>
              <v-col cols="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/marketplace-webstore/myntra.png"
                  class="img"
                  contain
                />
              </v-col>
            </v-row>
          </v-col>
        </v-col>
      </v-row>

      <!-- Mobile Layout End -->

      <!-- Shipping Integrations -->

      <v-row no-gutters class="main-shp-int">
        <v-col
          cols="12"
          sm="12"
          md="6"
          class="main-title-container px-0 pr-md-6 py-10"
        >
          <h1>
            Shipping <br />
            Integrations
          </h1>
          <p>
            Automate waybill generation, shipment tracking and NDR management
            across 20+ shipping partners. Our integrations also allow you
            schedule hyperlocal deliveries from your fulfillment centers and
            monitor deliveries in real time.
          </p>
        </v-col>
        <v-col
          cols="12"
          sm="12"
          md="6"
          class="shp-int-logos pl-md-6"
          v-if="!isSmallDevice"
        >
          <v-row
            no-gutters
            class="logos-container-1 mb-6 mt-12"
            justify="space-between"
          >
            <v-col cols="3" md="2" sm="3" class="logos">
              <v-img
                src="/Solutions/technology/company-logos/shipping-integrations/shiprocket.png"
                class="img"
                contain
              />
            </v-col>
            <v-col cols="3" md="2" sm="3" class="logos">
              <v-img
                src="/Solutions/technology/company-logos/shipping-integrations/bluedart.png"
                class="img"
                contain
              />
            </v-col>

            <v-col cols="3" md="2" sm="3" class="logos">
              <v-img
                src="/Solutions/technology/company-logos/shipping-integrations/dtdc.png"
                class="img"
                contain
              />
            </v-col>
            <v-col cols="3" md="2" sm="3" class="logos">
              <v-img
                src="/Solutions/technology/company-logos/shipping-integrations/delhivery.png"
                class="img"
                contain
              />
            </v-col>
            <v-col cols="3" md="2" sm="3" class="logos">
              <v-img
                src="/Solutions/technology/company-logos/shipping-integrations/far-eye.png"
                class="img"
                contain
              />
            </v-col>
          </v-row>
          <v-row no-gutters class="logos-container-2" justify="end">
            <v-col cols="3" md="2" sm="3" class="logos">
              <v-img
                src="/Solutions/technology/company-logos/shipping-integrations/shipsy.png"
                class="img"
                contain
              />
            </v-col>
          </v-row>
        </v-col>
        <!-- Mobile Layout Start -->
        <v-col class="main-si" v-if="isSmallDevice">
          <v-col cols="12" class="shp-int-logos">
            <v-row no-gutters class="logos-container-1">
              <v-col cols="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/shipping-integrations/shiprocket.png"
                  class="img"
                  contain
                />
              </v-col>
              <v-col cols="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/shipping-integrations/bluedart.png"
                  class="img"
                  contain
                />
              </v-col>

              <v-col cols="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/shipping-integrations/dtdc.png"
                  class="img"
                  contain
                />
              </v-col>
              <v-col cols="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/shipping-integrations/delhivery.png"
                  class="img"
                  contain
                />
              </v-col>
              <v-col cols="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/shipping-integrations/far-eye.png"
                  class="img"
                  contain
                />
              </v-col>
              <v-col cols="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/shipping-integrations/shipsy.png"
                  class="img"
                  contain
                />
              </v-col>
            </v-row>
          </v-col>
        </v-col>
      </v-row>

      <!-- Mobile End -->
      <!-- ERP  -->
      <v-row no-gutters class="main-erp">
        <v-col
          cols="12"
          sm="12"
          md="6"
          class="main-title-container px-0 py-10 pr-md-6"
        >
          <h1>ERP</h1>
          <p>
            Manage your omnichannel business easily with accounting and ERP
            integrations. One-click integrations to automate your tax engine,
            reconciliations and data transfers.
          </p>
        </v-col>
        <v-col
          cols="12"
          sm="12"
          md="6"
          class="erp-logos pl-md-6"
          v-if="!isSmallDevice"
        >
          <v-row
            no-gutters
            class="logos-container-1 mb-6 mt-6"
            justify="space-between"
          >
            <v-col cols="3" md="2" sm="3" class="logos">
              <v-img
                src="/Solutions/technology/company-logos/erp/sap.png"
                class="img"
                contain
              />
            </v-col>
            <v-col cols="3" md="2" sm="3" class="logos">
              <v-img
                src="/Solutions/technology/company-logos/erp/oracle.png"
                class="img"
                contain
              />
            </v-col>

            <v-col cols="3" md="2" sm="3" class="logos">
              <v-img
                src="/Solutions/technology/company-logos/erp/zoho.png"
                class="img"
                contain
              />
            </v-col>
            <v-col cols="3" md="2" sm="3" class="logos">
              <v-img
                src="/Solutions/technology/company-logos/erp/quickbooks.png"
                class="img"
                contain
              />
            </v-col>
            <v-col cols="3" md="2" sm="3" class="logos">
              <v-img
                src="/Solutions/technology/company-logos/erp/microsoft-dynamics.png"
                class="img"
                contain
              />
            </v-col>
          </v-row>
          <v-row no-gutters class="logos-container-2" justify="end">
            <v-col cols="3" md="2" sm="3" class="logos mx-7">
              <v-img
                src="/Solutions/technology/company-logos/erp/xero.png"
                class="img"
                contain
              />
            </v-col>
            <v-col cols="3" md="2" sm="3" class="logos">
              <v-img
                src="/Solutions/technology/company-logos/erp/busy.png"
                class="img"
                contain
              />
            </v-col>
          </v-row>
        </v-col>
        <!-- Mobile Layout Start -->
        <div class="main-erp" v-if="isSmallDevice">
          <div class="erp-logos">
            <v-row no-gutters class="logos-container-1" justify="end">
              <v-col cols="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/erp/sap.png"
                  class="img"
                  contain
                />
              </v-col>
              <v-col
                cols="3"
                class="logos"
                style="padding-right: 12px; padding-bottom: 12px"
              >
                <v-img
                  src="/Solutions/technology/company-logos/erp/oracle.png"
                  class="img"
                  contain
                />
              </v-col>

              <v-col
                cols="3"
                class="logos"
                style="padding-right: 12px; padding-bottom: 12px"
              >
                <v-img
                  src="/Solutions/technology/company-logos/erp/zoho.png"
                  class="img"
                  contain
                />
              </v-col>
              <v-col
                cols="3"
                class="logos"
                style="padding-right: 12px; padding-bottom: 12px"
              >
                <v-img
                  src="/Solutions/technology/company-logos/erp/quickbooks.png"
                  class="img"
                  contain
                />
              </v-col>
              <v-col
                cols="3"
                class="logos"
                style="padding-right: 12px; padding-bottom: 12px"
              >
                <v-img
                  src="/Solutions/technology/company-logos/erp/microsoft-dynamics.png"
                  class="img"
                  contain
                />
              </v-col>
              <v-col
                cols="3"
                class="logos"
                style="padding-right: 12px; padding-bottom: 12px"
              >
                <v-img
                  src="/Solutions/technology/company-logos/erp/xero.png"
                  class="img"
                  contain
                />
              </v-col>
              <v-col cols="3" class="logos">
                <v-img
                  src="/Solutions/technology/company-logos/erp/busy.png"
                  class="img"
                  contain
                />
              </v-col>
            </v-row>
          </div>
        </div>
        <!-- Mobile End -->
      </v-row>
    </v-row>
  </v-container>
</template>

<script>
import ConnectModal from "../../../ModalForm/ConnectModal.vue";

export default {
  components: {
    ConnectModal,
  },
  data() {
    return {
      isSmallDevice: false,
      showModal: false,
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
.integrations-main {
  height: auto;

  .main_content {
    height: auto;
    padding: 4% 6%;

    .main_left_content {
      height: auto;
      position: relative;

      .main_title {
        width: 100%;
        display: flex;
        align-items: baseline;

        h1 {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 400;
          font-size: 42px;
          line-height: 57px;
          text-align: center;
          color: #ffffff;
          text-align: left;
        }
      }

      .content-header {
        h1 {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 100;
          font-size: 32px;
          line-height: 44px;
          color: #ffffff;
        }
      }

      .content-para {
        p {
          font-family: "Outfit";
          font-style: normal;
          font-weight: 300;
          font-size: 16px;
          line-height: 20px;
          color: #9c9c9c;
        }
      }

      .content-button {
        display: flex;
        margin: 10% 0 0 0;
        position: absolute;
        bottom: 0;

        .button {
          display: flex;
          height: 40px;
          width: 170px;
          border-radius: 73px;
          text-transform: initial;
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 400;
          font-size: 18px;
          line-height: 25px;
          color: #ffffff;
          border: none;
          letter-spacing: 0px;

          span {
            font-weight: 500 !important;
          }

          &.primary {
            background-color: #00a699;
            box-shadow: inset 0 0 0 0 #00a699;
            transition: color 0.3s ease-in-out, box-shadow 0.3s ease-in-out;

            &:hover {
              box-shadow: inset 178px 0 0 0 #ffffff;
              color: #000000;
            }
          }
        }
      }
    }

    .main_right_image {
      height: auto;

      img {
        width: 100%;
        height: 100%;
      }
    }
  }

  .int-wrapper {
    padding: 4% 6%;
    background: #f3f3f5;

    .automate-main,
    .main-shp-int,
    .main-erp {
      height: auto;

      .main-title-container {
        h1 {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 400;
          font-size: 32px;
          line-height: 44px;
          color: #0c0c0c;
        }

        p {
          font-family: "Outfit";
          font-style: normal;
          font-weight: 300;
          font-size: 16px;
          line-height: 20px;
          color: #313131;
          margin-top: 1rem;
        }
      }

      .main-mkt-wbs,
      .main-si,
      .main-erp {
        display: flex;

        .main-title {
          h1 {
            font-family: "Noto Serif";
            font-style: normal;
            font-weight: 400;
            font-size: 32px;
            line-height: 44px;
            color: #1e1e1e;
          }

          p {
            font-family: "Outfit";
            font-style: normal;
            font-weight: 300;
            font-size: 16px;
            line-height: 20px;
            color: #313131;
            margin-top: 1rem;
          }
        }

        .mkt-wbs-logos {
          height: auto;
          display: flex;
          flex-direction: column;
          justify-content: space-around;
        }

        .shp-int-logos {
          height: auto;
          display: flex;
          flex-direction: column;
          justify-content: space-around;
        }

        .erp-logos {
          height: auto;
          display: flex;
          flex-direction: column;
          justify-content: space-around;
        }
      }
    }
  }
}

@media screen and (max-width: 850px) {
  .main_title {
    h1 {
      font-size: 30px;
    }
  }
  .main-title-container h1 {
    font-size: 24px !important;
  }
  .col-3 {
    padding-right: 12px !important;
    padding-bottom: 12px !important;
  }
  .integrations-main {
    .main_content {
      .main_left_content {
        .main_title {
          h1 {
            font-weight: 500 !important;
            font-size: 30px !important;
            line-height: 2rem !important;
          }
        }

        .content-header {
          h1 {
            font-weight: 100 !important;
            font-size: 24px !important;
            line-height: 30px;
          }
        }

        .main_right_image {
          img {
            width: 100% !important;
            height: 100% !important;
          }
        }

        .content-para {
          padding-top: 2rem !important;

          p {
            font-size: 16px !important;
            line-height: 20px !important;
          }
        }

        .content-button {
          padding: 5% 20% !important;
          justify-content: center;
          position: unset;

          .button {
            height: 2.5rem !important;
            width: 12rem !important;
            font-size: 14px !important;
            line-height: 20px !important;
            font-weight: 300 !important;
          }
        }
      }
    }

    .automate-main,
    .main-shp-int {
      .main-title-container {
        h1 {
          font-size: 24px !important;
          line-height: 2.063rem !important;
        }
      }

      .main-mkt-wbs,
      .main-si,
      .main-erp {
        display: flex !important;
        height: auto !important;
        flex-direction: column !important;

        .main-title {
          h1 {
            font-size: 24px !important;
            line-height: 1.875rem !important;
          }

          p {
            font-size: 16px !important;
            line-height: 20px !important;
          }
        }

        .mkt-wbs-logos {
          .logos-container-1 {
            justify-content: flex-end !important;
          }
        }

        .shp-int-logos {
          .logos-container-1 {
            justify-content: flex-end !important;
          }
        }

        .erp-logos {
          .logos-container-1 {
            justify-content: flex-end !important;
          }
        }
      }
    }
  }
}
</style>
