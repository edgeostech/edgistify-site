<template>
  <div class="hand-anim">
    <div class="content-container">
      <div class="left-section-container">
        <div class="vid-container">
          <!-- <video autoplay muted loop class="video-player">
            <source
              src="https://edgistify.s3.ap-south-1.amazonaws.com/media/website2023_video/hand_video.mp4"
              type="video/mp4"
            />
          </video> -->

          <v-img
              :src="`/Homepage/digital-age-supply-chain-management.gif.gif`"
              alt="Digital age supply chain management - animated image"
              cover
              class="video-player"
            ></v-img>


        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.hand-anim {
  display: flex;
  height: auto;
  align-items: center;
  justify-content: center;
  margin-left: -14%;
  .content-container {
    display: flex;
    width: 100%;
    height: auto;
    align-items: center;
    justify-content: space-between;

    .left-section-container {
      display: flex;
      width: 100%;
      height: auto;
      flex-direction: column;
      justify-content: center;
      background-color: #0c0c0c;
      // padding-right: 4rem;

      .vid-container {
        display: flex;
        width: 90%;
        height: auto;
        align-items: center;
        video {
          width: 180%;
          height: auto;
          position: static;
          margin: 30% 0 0 0%;
        }
      }
    }
  }
}

@media (max-width: 850px) {
  .hand-anim {
    display: flex;
    width: 100%;
    height: auto;
    align-items: center;
    justify-content: center;
    background: #0c0c0c !important;

    .content-container {
      display: flex;
      width: 100%;
      height: auto;
      align-items: center;
      justify-content: space-between;

      .left-section-container {
        display: flex;
        width: 100% !important;
        height: 180px !important;
        flex-direction: column;
        justify-content: center;
        background: #0c0c0c !important;

        .vid-container {
          display: flex;
          width: 100% !important;
          height: auto !important;
          align-items: center;
          background: #0c0c0c !important;
          .video-player {
            width: 82% !important;
            height: auto !important;
          }

          video {
            height: auto !important;
            position: static !important;
            left: 0rem !important;
            top: 0rem !important;
            padding-top: 0% !important;
          }
        }
      }
    }
  }
}
</style>

<script>
import aosMixin from "~/mixins/aos";

export default {
  mixins: [aosMixin],
};
</script>
