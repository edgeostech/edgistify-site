<template>
  <div class="hand-anim">
    <div class="content-container">
      <div class="left-section-container">
        <div class="vid-container">
          <!-- <v-img src="/Homepage/OurExperties/hand.png" height="190px" contain>
          </v-img> -->
          <video autoplay muted loop>
            <source src="/Homepage/HandAnimation/hand_video.mp4" type="video/mp4" />
          </video>
        </div>
      </div>
      <div class="right-section-container">
        <div class="action-container" data-aos="fade-up" data-aos-once="true" data-aos-easing="ease-in"
          data-aos-duration="1300">
          <v-btn class="button primary">Talk to an Expert</v-btn>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.hand-anim {
  display: flex;
  width: 100%;
  height: 220px;
  align-items: center;
  justify-content: center;
  background-color: #0c0c0c;
  // background-image: url("/Common/background-grid-top.png");
  // background-position: top;
  // background-size: contain;

  .content-container {
    display: flex;
    width: 100%;
    height: 100%;
    align-items: center;
    justify-content: space-between;

    .left-section-container {
      display: flex;
      width: 50%;
      height: 250%;
      flex-direction: column;
      justify-content: center;
      // padding-right: 4rem;

      .vid-container {
        display: flex;
        width: 50%;
        height: 250%;
        align-items: center;
        // margin-bottom: 35px;
        // margin-top: 47px;
        // padding-left: 30px;
        // align-items: center;
      }
    }
  }

  .right-section-container {
    display: flex;
    width: 50%;
    height: 200%;
    flex-direction: column;
    justify-content: center;

    .action-container {
      display: flex;
      align-items: center;
      width: 50%;
      height: 250%;
      padding-left: 180px;
      background-color: #0c0c0c;

      .button {
        display: flex;
        height: 42px;
        align-items: center;
        justify-content: center;
        border: 1px solid #00a699;
        border-radius: 40px;
        color: #fff;
        padding: 10px 40px;
        font-family: "Noto Serif";
        text-transform: capitalize;
        font-size: 16px;

        .v-btn__content {
          font-weight: bold;
          font-family: "Noto Serif";
        }

        &.primary {
          background-color: #00a699;

          &:hover {
            background-color: #008b80;
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
}
</style>

<script>
import aosMixin from "~/mixins/aos";

export default {
  mixins: [aosMixin],
};
</script>
