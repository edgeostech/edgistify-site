<template>
  <v-container fluid class="ecommerce-fulfillment-main pa-0">
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-row id="e_commerce" no-gutters>
      <div class="main_title">
        <h1>E-commerce Fulfillment</h1>
      </div>
    </v-row>
    <v-row class="main_content pa-0" no-gutters>
      <v-col class="main_left_image pa-0 pr-md-16 pb-12" sm="12" md="6">
        <v-img
          src="/Solutions/warehousing/e-commerce-fulfillment-services.jpg.jpg"
          alt="Efficient e-commerce fulfillment services for your business needs with streamlined processes and on-time deliveries"
          contain
        />
      </v-col>
      <v-col class="main_right_content pa-0" sm="12" md="6">
        <div class="content-header">
          <h1>Deliver on Time, Every Time</h1>
        </div>
        <div class="content-para">
          <p>
            Scalable e-commerce fulfilment designed as per your business needs.
            Process a significant number of orders within a short time and
            deliver in every part of India. Store inventory closest to customers
            and seamlessly manage your inventory and order fulfilment operations
            from our fulfilment centres. Manage and gain complete visibility on
            inbound, storage, QC, packaging and outbound operations.
          </p>
        </div>
        <div class="content-para-list">
          <div class="list">Flexibility and Scalability</div>
          <div class="list">Customization</div>
          <div class="list">Cost Effectiveness</div>
          <div class="list">TAT Accuracy</div>
          <div class="list">Proficient Manpower</div>
        </div>
        <div class="content-button">
          <v-btn
            class="button bg-white"
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-anchor=".content-para"
            data-aos-duration="1000"
            @click="showModal = true"
            >Get in Touch</v-btn
          >
        </div>
      </v-col>
    </v-row>
    <v-row class="main_point_detail" no-gutters>
      <v-col class="left_main pr-16 pb-12" sm="12" md="6">
        <!-- <v-img
            src="/Solutions/warehousing/warehouse-material-handling-forklift.png"
            cover
          /> -->
      </v-col>
      <v-col class="right_main mt-12 mb-12" sm="12" md="6">
        <ul class="right_main_container">
          <li class="right_main_title">
            <div class="right_main_top">
              <h1>Warehousing</h1>
              <img
                src="/Common/right-arrow-v2.png"
                contain
                class="right-arrow"
              />
              <img src="/Common/down-grp.png" contain class="down-arrow" />
            </div>
            <ul class="right_main_description">
              <li>On demand warehousing</li>
              <li>Fully-equipped facilities for e-commerce operations</li>
              <li>24x7 CCTV surveillance</li>
            </ul>
          </li>
          <li class="right_main_title">
            <div class="right_main_top">
              <h1>Inventory Management</h1>
              <img
                src="/Common/right-arrow-v2.png"
                contain
                class="right-arrow"
              />
              <img src="/Common/down-grp.png" contain class="down-arrow" />
            </div>
            <ul class="right_main_description">
              <li>Stock inventory near your customers</li>
              <li>Real-time stock visibility and stock-out alerts</li>
              <li>Shared inventory pool for all channels</li>
            </ul>
          </li>
          <li class="right_main_title">
            <div class="right_main_top">
              <h1>Order Management</h1>
              <img
                src="/Common/right-arrow-v2.png"
                contain
                class="right-arrow"
              />
              <img src="/Common/down-grp.png" contain class="down-arrow" />
            </div>
            <ul class="right_main_description">
              <li>Intelligent order routing</li>
              <li>Omnichannel integrated fulfilment</li>
              <li>
                Seamless Integration with top couriers, ERPs, CRM and accounting
                tools
              </li>
            </ul>
          </li>
          <li class="right_main_title">
            <div class="right_main_top">
              <h1>Order Picking and Packing</h1>
              <img
                src="/Common/right-arrow-v2.png"
                contain
                class="right-arrow"
              />
              <img src="/Common/down-grp.png" contain class="down-arrow" />
            </div>
            <ul class="right_main_description">
              <li>Trained and equipped team of pickers and packers</li>
              <li>Customisation and Personalisation services</li>
              <li>99.9% accuracy in picking and packing</li>
            </ul>
          </li>
          <li class="right_main_title">
            <div class="right_main_top">
              <h1>Shipping and Logistics</h1>
              <img
                src="/Common/right-arrow-v2.png"
                contain
                class="right-arrow"
              />
              <img src="/Common/down-grp.png" contain class="down-arrow" />
            </div>
            <ul class="right_main_description">
              <li>Pan-India Courier and Transport Network</li>
              <li>Hyperlocal Delivery in 2 hours to 24 hours</li>
              <li>B2B Logistics</li>
            </ul>
          </li>
          <li class="right_main_title">
            <div class="right_main_top">
              <h1>Returns</h1>
              <img
                src="/Common/right-arrow-v2.png"
                contain
                class="right-arrow"
              />
              <img src="/Common/down-grp.png" contain class="down-arrow" />
            </div>
            <ul class="right_main_description">
              <li>Complete control over Non-deliveries and Returns</li>
              <li>Recirculate RTO and returns in the shortest time</li>
            </ul>
          </li>
        </ul>
      </v-col>
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
      showModal: false,
    };
  },
};
</script>

<style lang="scss" scoped>
.ecommerce-fulfillment-main {
  .main_title {
    width: 100%;
    display: flex;
    background: #00a699;
    justify-content: baseline;
    padding: 0 6% !important;
    align-items: center;

    h1 {
      font-family: "Noto Serif";
      font-style: normal;
      font-weight: 400;
      font-size: 42px;
      line-height: 57px;
      color: #ffffff;
      padding: 12px;
    }
  }

  .main_content {
    padding: 0 6% !important;

    .main_left_image {
      margin: 50px 0 0 0;
    }

    .main_right_content {
      display: flex;
      flex-direction: column;
      margin: 50px 0 0 0;
      position: relative;

      .content-header {
        width: 100%;

        h1 {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 300;
          font-size: 32px;
          line-height: 40px;
          color: #1e1e1e;
        }
      }

      .content-para {
        width: 100%;
        margin-top: 1rem;
        padding-right: 2.5rem;

        p {
          font-family: "Outfit";
          font-style: normal;
          font-weight: 300;
          font-size: 16px;
          line-height: 20px;
          color: #313131;
        }
      }

      .content-para-list {
        width: 100%;
        margin-top: 1rem;
        border-left: 1px solid #313131;
        transform: rotate(0deg);

        .list {
          font-family: "Outfit";
          font-style: normal;
          font-weight: 300;
          font-size: 16px;
          line-height: 24px;
          margin-left: 1rem;
          color: #1e1e1e;
        }
      }

      .content-button {
        margin-bottom: 48px;
        margin-top: 48px;
        position: absolute;
        bottom: 0;

        .button {
          display: flex;
          width: 11rem;
          height: 3rem;
          //border: 1px solid #00a699;
          border-radius: 73px;
          color: #fff;
          font-family: "Noto Serif";
          text-transform: initial;
          font-style: normal;
          font-size: 18px;
          font-weight: 700;
          line-height: 25px;
          border: none;
          letter-spacing: 0px;

          // span {
          //    font-weight: 500 !important;
          // }

          &.primary {
            background-color: #00a699;
            box-shadow: inset 0 0 0 0 #00a699;
            transition: color 0.3s ease-in-out, box-shadow 0.3s ease-in-out;

            &:hover {
              box-shadow: inset 178px 0 0 0 #000000;
              color: #ffffff;
            }
          }
        }
      }
    }
  }

  .main_point_detail {
    background: #0c0c0c;
    padding: 0 6%;

    .left_main {
      .v-image {
        width: 70%;
      }
    }

    .right_main {
      .right_main_container {
        background: #0c0c0c;
        padding-left: 0 !important;

        .right_main_title:hover .right_main_description {
          display: flex;
        }

        .right_main_title:hover .down-arrow {
          display: flex;
        }

        .down-arrow {
          display: none;
        }

        .right-arrow {
          display: block;
        }

        .right_main_title:hover .right-arrow {
          display: none;
        }

        .right_main_title:hover {
          border-bottom: 1px solid #00a699;
        }

        .right_main_title {
          display: flex;
          flex-direction: column;
          align-items: center;
          justify-content: space-between;
          width: 100%;
          border-bottom: 1px solid rgba(255, 255, 255, 0.5);
          margin: 12px 20px 10px 0;
          padding: 0 15px 5px 15px;
          cursor: pointer;

          // height: 50%;

          .right_main_top {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 100%;
          }

          .right_main_description {
            list-style-type: none;
            display: none;
            flex-direction: column;
            width: 100%;
            height: auto;
            margin: 1em 0 1em 0;

            li {
              font-family: "Outfit";
              font-style: normal;
              font-weight: 300;
              font-size: 15px;
              line-height: 20px;
              transition: all 0.3s ease-in-out;

              color: #ffffff;
            }

            li::before {
              content: "•";
              color: white;
              display: inline-block;
              width: 1em;
              margin-left: 0em;
            }
          }

          h1 {
            font-family: "Outfit";
            font-style: normal;
            font-weight: 400;
            font-size: 26px;
            line-height: 40px;
            // margin: 0 0 5px 15px;

            color: #ffffff;
          }

          &:hover {
            color: #ffffff;
          }
        }
      }
    }
  }
}

@media (max-width: 850px) {
  .main_title {
    h1 {
      font-size: 30px !important;
    }
  }

  .content-header {
    h1 {
      font-size: 24px !important;
    }
  }
  .main_right_content {
    margin: 0 !important;
  }

  .left_main {
    display: none;
  }
  .main_content {
    flex-wrap: wrap;
    height: auto !important;

    .main_left_image,
    .main_right_content {
      .content-para {
        margin-top: 30px !important;
        height: auto !important;
        padding-right: 0rem !important;
      }

      .content-button {
        margin: 48px auto !important;
        position: unset !important;
      }
    }
  }

  .v-image {
    height: auto !important;
    margin-left: 0 !important;
  }

  .main_point_detail {
    height: auto !important;
    flex-wrap: wrap !important;

    .left_main,
    .right_main {
      width: 100vw !important;
    }
  }
}
</style>
