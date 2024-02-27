<template>
  <v-container fluid class="team-container">
    <v-row class="team-wrapper" id="our-team" no-gutters justify="space-between">
      <v-col sm="12" class="img-div">
        <v-img src="/Company/edgistify-team.jpg.jpg" alt="Edgistify team of supply chain specialists working together to provide innovative solutions for businesses" class="img"></v-img>
      </v-col>
      <v-col class="join-us">
        <div class="text-wrapper">
          <h1>
            Join Us in Our Mission to Transform Supply Chain
          </h1>
        </div>

        <nuxt-link :to="{ path: '/careers/exciting-opportunities-join-the-team-edgistify', hash: '#careers-container' }" style="text-decoration: none; color: inherit"
          @click.native="scrollToLocation" class="join-us-btn">
          <span class="btn bg-white">Join Us</span>
        </nuxt-link>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup></script>

<style lang="scss" scoped>
.btn {
  padding: 11.5px 26px;
  font-family: "Noto Serif";
  gap: 10px;
  height: 48px;
  background: #00a699;
  border-radius: 38px;
  color: white;
}

.team-container {
  width: 100%;
  height: auto;
  background: #ffff;
  padding: 0 6%;
  padding-bottom: 6%;

  .team-wrapper {
    display: flex;
    flex-direction: column;
    margin-top: 4rem;

    .img-div {
      width: 100%;

      .img {
        height: 533px;
      }
    }

    .join-us {
      width: 100%;
      display: flex;
      margin-top: 2rem;
      justify-content: space-between;
      align-items: center;

      .text-wrapper {
        display: flex;
        justify-content: baseline;
        align-items: center;

        h1 {
          font-family: "Noto Serif";
          font-style: normal;
          font-weight: 500;
          font-size: 32px;
          line-height: 40px;
          color: #0c0c0c;
        }
      }

      .btn-container {
        display: flex;
        justify-content: end;
        align-items: center;

        .btn {
          width: 150px;
          height: 42px;
          background: #00a699;
          border-radius: 44px;
          text-align: center;
          padding-top: 0.75rem;
          color: #ffffff;
          text-transform: capitalize;
        }
      }
    }
  }
}

@media screen and (max-width: 850px) {
  .team-container {
    width: 100%;
    height: auto !important;
    background: #ffff;
    padding: 0 30px !important;

    .team-wrapper {
      display: flex;
      flex-direction: column;
      margin: 0rem !important;

      .img-div {
        width: 100%;

        .img {
          width: 100% !important;
          height: 100% !important;
        }
      }

      .join-us {
        margin-bottom: 2rem !important;
        flex-direction: column !important;
        align-items: center !important;

        .text-wrapper {
          h1 {
            width: 100% !important;
            font-size: 1.5rem !important;
            line-height: 2rem !important;
            color: #0c0c0c !important;
          }
        }

        .join-us-btn {
          padding-top: 10% !important;
        }

        .btn-container {
          width: 100% !important;
          margin-top: 8% !important;

          .btn {
            width: 150px;
            height: 42px;
            background: #00a699;
            border-radius: 44px;
            text-align: center;
            padding-top: 0.75rem;
          }
        }
      }
    }
  }
}
</style>
