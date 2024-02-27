<template>
  <v-container
    fluid
    class="solutions-transportation-container pa-0"
    id="solutions-transportation-container"
  >
    <ConnectModal v-show="showModal" @close-modal="showModal = false" />
    <v-row class="head-cover" no-gutters>
      <v-col sm="12" md="6" class="ma-0">
        <div class="banner-left">
          <h1>Optimizing Every Mile with Our Logistics Solutions</h1>

          <v-col class="dashboard_content" style="padding: 0">
            <p>
              With the growth of e-commerce, efficient management of supply
              chain has become more important than ever to meet customer
              expectations. Get end-to-end logistics solutions, including First
              Mile, Mid Mile, and Last Mile delivery, to help businesses deliver
              products to their customers efficiently and on time.
            </p>
          </v-col>

          <v-col class="title_button pa-0">
            <v-btn
              class="button bg-white"
              data-aos="fade-up"
              data-aos-once=" true"
              data-aos-easing="ease-in"
              data-aos-anchor=".title"
              data-aos-duration="1000"
              @click="showModal = true"
              >Get in Touch</v-btn
            >
          </v-col>
        </div>
      </v-col>
      <v-col sm="12" md="6" class="right-head-cover pa-0">
        <v-img
          :src="`/Solutions/warehousing/transporatation-first-mid-last-mile-operations.gif.gif`"
          alt=""
          aspect-ratio="1"
          cover
          class="bg-grey-lighten-2 image-gif"
        ></v-img>
      </v-col>
    </v-row>
    <FirstMile />
    <MiddleMile />
    <LastMile />
    <EdgistifyForm />
  </v-container>
</template>

<script>
import aosMixin from "~/mixins/aos";
import FirstMile from "../../components/Solutions/Transportation/FirstMile/FirstMile.vue";
import MiddleMile from "../../components/Solutions/Transportation/MiddleMile/MiddleMile.vue";
import LastMile from "../../components/Solutions/Transportation/LastMile/LastMile.vue";
import EdgistifyForm from "../../components/EdgistifyForm/EdgistifyForm.vue";
import ConnectModal from "../../components/ModalForm/ConnectModal.vue";

export default {
  components: {
    FirstMile,
    MiddleMile,
    LastMile,
    EdgistifyForm,
    ConnectModal,
  },
  mixins: [aosMixin],
  data() {
    return {
      showModal: false,
    };
  },
  head() {
    return {
      title: "Edgitify Logistics Channel for Warehousing and Transportation Streamline Your Operations"
    };
  }
};
</script>

<style lang="scss" scoped>


.solutions-transportation-container {
  height: auto;
  background-color: #0c0c0c;
  padding-top: 92px !important;

  .dashboard_content {
    width: 100%;

    p {
      font-family: "Outfit";
      font-style: normal;
      font-weight: 300;
      font-size: 16px;
      line-height: 20px;
      color: #0c0c0c;
    }
  }

  .head-cover {
    .banner-left {
      height: 100%;
      display: flex;
      padding: 4% 12%;
      flex-direction: column;
      justify-content: center;
      background-color: #ffffff;

      h1 {
        font-family: "Noto Serif";
        font-style: normal;
        font-weight: 300;
        font-size: 46.6116px;
        line-height: 63px;
        color: #161616;
        margin-bottom: 6%;
      }

      .button {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        padding: 11.5px 26px;
        width: 11rem;
        font-family: "Noto Serif";
        height: 48px;
        background: #00a699;
        border-radius: 38px;
        color: white;

        // span {
        //    font-weight: 500 !important;
        // }

        &.btn {
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

    .right-head-cover {
      // display: flex;
      // width: 50%;
      height: auto;

      .head_image {
        width: 100%;

        video {
          // width: 50vw;
          height: auto;
          object-fit: cover;
        }
      }
    }
  }

  .empty-div {
    width: 100%;
    height: 600px;
    background: #ffffff;
  }
}

@media (max-width: 850px) {
  .solutions-transportation-container {
  padding-top: 0 !important;}
  .title_header {
    height: auto !important;
  }

  .head-cover {
    flex-wrap: wrap;
    height: auto !important;
    flex-direction: column-reverse;

    .banner-left {
      padding: 0 6% !important;
      height: auto !important;

      h1 {
        font-family: "Noto Serif" !important;
        font-style: normal !important;
        font-weight: 300 !important;
        font-size: 2rem !important;
        line-height: 2rem !important;
        color: #1e1e1e !important;
        margin: 6% 0 !important;
      }

      .title_button {
        justify-content: center;
        display: flex;
        margin: 0 0 48px 0;
      }
    }

    .right-head-cover {
      .head_image {
        width: 100vw !important;
        height: auto !important;

        video {
          width: 100vw !important;
        }
      }
    }
  }
}
</style>
