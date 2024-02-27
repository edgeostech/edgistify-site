<template>
  <v-app>
    <div class="mainpage">
      <Header v-if="!isSmallDevice" />
      <MobileHeader v-if="isSmallDevice" />
      <Nuxt />
      <Footer />
    </div>
  </v-app>
</template>

<style lang="scss">
.mainpage {
  width: 100%;
  max-width: 100%;
  overflow-x: hidden;
}

// .canvas {
//   z-index: 1 !important;
// }
</style>

<script>
import Header from "../components/header/Header.vue";
import MobileHeader from "../components/MobileHeader/MobileHeader.vue";
import Footer from "../components/footer/Footer.vue";

export default {
  components: {
    Header,
    Footer,
    MobileHeader,
  },
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
