<template>
  <v-container fluid class="our-services-container pa-0">
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-col
      class="section-container px-0"
      data-aos="fade-up"
      data-aos-once="true"
      data-aos-easing="ease-in"
      data-aos-duration="800"
    >
      <v-col
        cols="5"
        sm="4"
        md="2"
        class="section"
        id="warehousing"
        :class="{ selected: selected === 'Warehousing' }"
        @click="() => toggleSelection('Warehousing', 'warehousing')"
      >
        <!-- <span>Logistics</span> -->
        <span>Warehousing</span>
      </v-col>
      <v-col
        cols="5"
        sm="4"
        md="2"
        class="section"
        id="same-day-delivery"
        :class="{ selected: selected === 'Same Day Delivery' }"
        @click="() => toggleSelection('Same Day Delivery', 'same-day-delivery')"
      >
        <!-- <span>Technology</span> -->
        <span>Same Day Delivery</span>
      </v-col>
      <v-col
        cols="5"
        sm="4"
        md="2"
        class="section"
        id="technology"
        :class="{ selected: selected === 'Technology' }"
        @click="() => toggleSelection('Technology', 'technology')"
      >
        <!-- <span>Fulfillment</span> -->
        <span>Technology</span>
      </v-col>
      <v-col
        cols="5"
        sm="4"
        md="2"
        class="section"
        id="transportation"
        :class="{ selected: selected === 'Transportation' }"
        @click="() => toggleSelection('Transportation', 'transportation')"
      >
        <span>Transportation</span>
      </v-col>
      <v-col
        cols="5"
        sm="4"
        md="2"
        class="section"
        id="consultancy"
        :class="{ selected: selected === 'Consulting' }"
        @click="() => toggleSelection('Consulting', 'consultancy')"
      >
        <span>Consulting</span>
      </v-col>
      <v-col
        cols="5"
        sm="4"
        md="2"
        class="section"
        id="support-services"
        :class="{ selected: selected === 'Support Services' }"
        @click="() => toggleSelection('Support Services', 'support-services')"
      >
        <span>Support Services</span>
      </v-col>
    </v-col>
    <v-col v-if="selected === 'Warehousing'" class="content-container px-0">
      <v-col cols="12" sm="12" md="6" class="content-text px-0 py-0">
        <v-col cols="12" sm="12" md="12" class="heading px-0">
          <h2
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="900"
          >
            <!-- Full suite of logistics services -->
            Integrated Warehousing Solutions
          </h2>
        </v-col>
        <v-col class="content px-0">
          <p
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="1000"
          >
            Experience smoother operations with our D2C, B2C, and B2B
            warehousing and fulfillment solutions.
          </p>
        </v-col>
        <v-col
          class="stat-container"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="1100"
        >
          <span>20 %</span>
          <p>Cost Per Order Reduction</p>
        </v-col>
        <div class="button_container">
          <v-btn
            class="button bg-black"
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="800"
            @click="showModal = true"
            >Get in touch</v-btn
          >
        </div>
      </v-col>
      <v-col cols="12" sm="12" md="6" class="content-text px-0">
        <nuxt-link
          :to="{
            path: '/solutions/warehouse-efficient-storage-and-management-solutions-edgistify',
          }"
          style="text-decoration: none; color: inherit"
        >
          <div class="content-image" style="margin-bottom: 4%">
            <div
              class="image-container"
              data-aos="fade-up"
              data-aos-once="true"
              data-aos-easing="ease-in"
              data-aos-duration="900"
            >
              <v-img
                src="/Homepage/OurServices/integrated-warehousing-solutions.jpg.jpg"
                contain
                alt="Integrated Warehousing Solutions for streamlined supply chain management"
              />
            </div>
          </div>
        </nuxt-link>
      </v-col>
    </v-col>
    <v-col
      v-if="selected === 'Same Day Delivery'"
      class="content-container px-0"
    >
      <v-col cols="12" sm="12" md="6" class="content-text px-0">
        <v-col cols="12" sm="12" md="12" class="heading px-0">
          <h2
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="900"
          >
            Swift Same-Day Delivery
          </h2>
        </v-col>
        <v-col
          class="content px-0"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="1000"
        >
          <p>
            Store your product near your customer and provide expeditious
            same-day delivery.
          </p>
        </v-col>
        <v-col
          class="stat-container"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="1100"
        >
          <span>98.5%</span>
          <p>TAT Accuracy</p>
        </v-col>
        <div class="button_container">
          <v-btn
            class="button bg-black"
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="800"
            @click="showModal = true"
            >Get in touch</v-btn
          >
        </div>
      </v-col>
      <v-col cols="12" sm="12" md="6" class="content-text px-0">
        <nuxt-link
          :to="{ path: '/solutions/same-day-delivery-fast-reliable-and-convenient-edgistify' }"
          style="text-decoration: none; color: inherit"
        >
          <div class="content-image">
            <div
              class="image-container"
              data-aos="fade-up"
              data-aos-once="true"
              data-aos-easing="ease-in"
              data-aos-duration="900"
            >
              <v-img
                src="/Homepage/OurServices/fast-same-day-delivery-ecommerce.jpg.jpg"
                alt="Ecommerce fulfillment with fast same-day delivery"
                contain
              />
            </div>
          </div>
        </nuxt-link>
      </v-col>
    </v-col>
    <v-col v-if="selected === 'Technology'" class="content-container px-0">
      <v-col cols="12" sm="12" md="6" class="content-text px-0">
        <v-col cols="12" sm="12" md="12" class="heading px-0">
          <h2
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="900"
          >
            Integrated Tech Solutions
          </h2>
        </v-col>
        <v-col class="content px-0">
          <p
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="1000"
          >
            A cloud based platform to manage all your inventory and warehouse
            operations. Automate and Integrate your marketplaces, carriers and
            enterprise suite.
          </p>
        </v-col>
        <v-col
          class="stat-container"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="1100"
        >
          <span>97 %</span>
          <p>Inventory Accuracy</p>
        </v-col>
        <div class="button_container">
          <v-btn
            class="button bg-black"
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="800"
            @click="showModal = true"
            >Get in touch</v-btn
          >
        </div>
      </v-col>
      <v-col cols="12" sm="12" md="6" class="content-text px-0">
        <nuxt-link
          :to="{
            path: '/solutions/tech-driven-supply-chain-and-warehouse-management-edgistify/',
          }"
          style="text-decoration: none; color: inherit"
        >
          <div class="content-image">
            <div
              class="image-container"
              data-aos="fade-up"
              data-aos-once="true"
              data-aos-easing="ease-in"
              data-aos-duration="900"
            >
              <v-img
                src="/Homepage/OurServices/integrated-technology-solutions.jpg.jpg"
                alt="Integrated Technology Solutions with Streamlined Supply Chain Management through Technology"
                contain
              />
            </div>
          </div>
        </nuxt-link>
      </v-col>
    </v-col>
    <v-col v-if="selected === 'Transportation'" class="content-container px-0">
      <v-col cols="12" sm="12" md="6" class="content-text px-0">
        <v-col cols="12" sm="12" md="12" class="heading px-0">
          <h2
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="900"
          >
            Reliable Transport Network
          </h2>
        </v-col>
        <v-col class="content px-0">
          <p
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="1000"
          >
            Fulfill your delivery commitments accurately and efficiently
            Pan-India.
          </p>
        </v-col>
        <v-col
          class="stat-container"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="1100"
        >
          <span>89% </span>
          <p>OTIF</p>
        </v-col>
        <br />
        <div class="button_container">
          <v-btn
            class="button bg-black"
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="800"
            @click="showModal = true"
            >Get in touch</v-btn
          >
        </div>
      </v-col>
      <v-col cols="12" sm="12" md="6" class="content-text px-0">
        <nuxt-link
          :to="{ path: '/solutions/edgitify-logistics-channel-for-warehousing-and-transportation-streamline-your-operations' }"
          style="text-decoration: none; color: inherit"
        >
          <div class="content-image">
            <div
              class="image-container"
              data-aos="fade-up"
              data-aos-once="true"
              data-aos-easing="ease-in"
              data-aos-duration="900"
            >
              <v-img
                src="/Homepage/OurServices/transport-network-optimization.jpg.jpg"
                alt="Smart technology solutions for transport network optimization"
                contain
              />
            </div>
          </div>
        </nuxt-link>
      </v-col>
    </v-col>
    <v-col v-if="selected === 'Consulting'" class="content-container px-0">
      <v-col cols="12" sm="12" md="6" class="content-text px-0">
        <v-col cols="12" sm="12" md="12" class="heading px-0">
          <h2
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="900"
          >
            Holistic Supply Chain Consulting
          </h2>
        </v-col>
        <v-col class="content px-0">
          <p
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="1000"
          >
            We help you operate more efficiently and effectively, gain
            competitive advantage, optimize your supply chain, and maximize
            business and shareholder value.
          </p>
        </v-col>
        <v-col
          class="stat-container"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="1100"
        >
          <span>99 %</span>
          <p>Client Satisfaction</p>
        </v-col>
        <div class="button_container">
          <v-btn
            class="button bg-black"
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="800"
            @click="showModal = true"
            >Get in touch</v-btn
          >
        </div>
      </v-col>
      <v-col cols="12" sm="12" md="6" class="content-text px-0">
        <nuxt-link
          :to="{ path: '/solutions/maximizing-efficiency-and-reducing-costs-consulting-of-supply-chain-management-edgistify' }"
          style="text-decoration: none; color: inherit"
        >
          <div class="content-image">
            <div
              class="image-container"
              data-aos="fade-up"
              data-aos-once="true"
              data-aos-easing="ease-in"
              data-aos-duration="900"
            >
              <v-img
                src="/Homepage/OurServices/supply-chain-consulting-services.jpg.jpg"
                alt="Supply chain consulting services - Business professionals discussing supply chain strategies and solutions"
                contain
              />
            </div>
          </div>
        </nuxt-link>
      </v-col>
    </v-col>
    <v-col
      v-if="selected === 'Support Services'"
      class="content-container px-0"
    >
      <v-col cols="12" sm="12" md="6" class="content-text px-0">
        <v-col cols="12" sm="12" md="12" class="heading px-0">
          <h2
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="900"
          >
            Augmented Supply Chain Solutions
          </h2>
        </v-col>
        <v-col class="content px-0">
          <p
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="1000"
          >
            Streamline your business operations with need-based storage,
            infrastructure and manpower solutions.
          </p>
        </v-col>
        <v-col
          class="stat-container"
          data-aos="fade-up"
          data-aos-once="true"
          data-aos-easing="ease-in"
          data-aos-duration="1100"
        >
          <span>99 %</span>
          <p>Storage Productivity</p>
        </v-col>
        <div class="button_container">
          <v-btn
            class="button bg-black"
            data-aos="fade-up"
            data-aos-once="true"
            data-aos-easing="ease-in"
            data-aos-duration="800"
            @click="showModal = true"
            >Get in touch</v-btn
          >
        </div>
      </v-col>
      <v-col cols="12" sm="12" md="6" class="content-text px-0">
        <nuxt-link
          :to="{ path: '/solutions/support-services-for-supply-chain-optimization-and-management-ensure-success-edgistify' }"
          style="text-decoration: none; color: inherit"
        >
          <div class="content-image">
            <div
              class="image-container"
              data-aos="fade-up"
              data-aos-once="true"
              data-aos-easing="ease-in"
              data-aos-duration="900"
            >
              <v-img
                src="/Homepage/OurServices/enhanced-supply-chain-planning.jpg.jpg"
                contain
                alt="Efficient supply chain planning to improve your business performance"
              />
            </div>
          </div>
        </nuxt-link>
      </v-col>
    </v-col>
  </v-container>
</template>

<style lang="scss" scoped>
.our-services-container {
  padding: 0 6% !important;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  background-color: #0c0c0c;
  padding: 0 94px;
  background-position: bottom;
  background-size: contain;

  .section-container {
    display: flex;
    height: auto;
    justify-content: center;

    .section {
      display: flex;
      width: 33.3%;
      height: 50%;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      color: #4e4e4e;

      border-bottom: 2px solid #4e4e4e;

      span {
        font-family: "Outfit";
        font-style: normal;
        font-weight: 500;
      }

      &:hover {
        color: #fff;
        border-color: #fff;
      }

      &.selected {
        border-color: #00a699;
        border-width: 3px;
        color: #00a699;
      }
    }
  }

  .content-container {
    display: flex;

    padding: 0 6%;

    .content-text {
      height: auto;
      flex-direction: column;
      position: relative;

      .heading {
        h2 {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 400;
          font-size: 42px;
          line-height: 50px;
          color: #fff;
        }
      }

      .content {
        display: flex;
      }

      p {
        font-size: 1rem;
        font-weight: 300;
        font-family: "Outfit";
        color: #fff;
      }

      .stat-container {
        height: fit-content;
        flex-direction: column;
        padding-left: 1rem;
        border-left: 5px solid #00a699;
        margin-top: 3%;
        justify-content: flex-start;

        span {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 500;
          font-size: 55px;
          line-height: 60px;
          color: #fff;
        }
      }
    }

    .content-image {
      margin-top: 2%;
      margin-bottom: 4%;
    }
  }

  .button_container {
    display: flex;
    width: 100%;
    height: fit-content;
    padding: 6% 3% 6% 0;
    position: absolute;
    bottom: 0;

    .button {
      width: 11.125rem;
      height: 3rem;
      align-items: center;
      justify-content: center;
      border: 1px solid #00a699;
      border-radius: 73px;
      color: #fff;
      font-family: "Noto Serif";
      text-transform: capitalize;
      line-height: 25px;
      font-size: 18px;
      font-weight: 500;
      border: none;
      letter-spacing: 0px;

      // .v-btn__content {
      //   font-weight: bold;
      //   font-family: "Noto Serif";
      // }

      span {
        font-weight: 500 !important;
      }

      &.primary {
        background-color: #00a699;
        box-shadow: inset 0 0 0 0 #00a699;
        transition: color 0.3s ease-in-out, box-shadow 0.3s ease-in-out;

        &:hover {
          background-color: #008b80;

          box-shadow: inset 178px 0 0 0 #fff;
          color: #000000;
        }
      }

      &.secondry {
        border: 1px solid #fff;
        background-color: transparent;

        &:hover {
          border-color: #008b80;
        }
      }
    }
  }
}

@media (max-width: 850px) {
  .our-services-container {
    display: block;
    height: auto;
    background-color: #0c0c0c;

    .section-container {
      width: 100% !important;
      overflow-x: scroll !important;
      overflow-y: hidden !important;
      scroll-behavior: smooth !important;
      justify-content: flex-start !important;
      scrollbar-width: none !important;
      -ms-overflow-style: none !important;

      .section {
        width: auto !important;
        white-space: nowrap !important;
        padding: 12px 30px !important;

        span {
          font-family: "Outfit" !important;
          font-style: normal !important;
          font-weight: 500 !important;
          font-size: 15px !important;
          line-height: 14px !important;
        }
      }
    }

    .content-container {
      flex-direction: column !important;

      .content-text {
        display: flex !important;
        width: 100% !important;
        height: 100% !important;

        .heading {
          h2 {
            font-weight: 400 !important;
            font-size: 30px !important;
            line-height: 35px !important;
          }
        }

        .content {
          width: 90% !important;

          p {
            font-weight: 300 !important;
            font-size: 14px !important;
            line-height: 20px !important;
          }
        }

        .stat-container {
          margin-top: 0px !important;

          span {
            font-weight: 500 !important;
            font-size: 30px !important;
            line-height: 40px !important;
            margin-bottom: 5px !important;
          }

          p {
            font-weight: 300 !important;
            font-size: 14px !important;
            line-height: 12px !important;
          }
        }
      }

      .content-image {
        height: auto !important;
        margin-top: 0rem !important;

        .image-container {
          padding-left: 0px !important;
        }
      }
    }

    .button_container {
      justify-content: center !important;
      margin-top: 1rem !important;
      position: unset;

      .button {
        width: 7.188rem !important;
        height: 1.938rem !important;
        font-size: 14px !important;
        line-height: 20px !important;
        font-weight: 300 !important;
      }
    }
  }
}
</style>

<script>
import aosMixin from "~/mixins/aos";
import ConnectModal from "../../ModalForm/ConnectModal.vue";

export default {
  components: {
    ConnectModal,
  },
  data() {
    return {
      selected: "Warehousing",
      showModal: false,
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
  mixins: [aosMixin],
  methods: {
    toggleSelection(section, label) {
      console.log("section:", section);
      console.log("this.selected:", this.selected);
      if (this.selected !== section) {
        this.selected = section;
        // document.getElementById(label).scrollLeft();
        if (this.isSmallDevice) {
          console.log("label:", label);
          console.log(
            "document.getElementById(label):",
            document.getElementById(label)
          );
          // element.scrollIntoView({ behavior: 'smooth'});
          const ele = document.getElementById(label);
          if (ele) {
            ele.scrollIntoView({
              behavior: "smooth",
              block: "nearest",
              inline: "start",
            });
          }
        }
      }
    },

    // findPosition (obj) {
    //   var currenttop = 0;
    //   if (obj.offsetParent) {
    //     do {
    //       currenttop += obj.offsetTop;
    //     } while ((obj = obj.offsetParent));
    //     return [currenttop];
    //   }
    // }
  },
};
</script>
