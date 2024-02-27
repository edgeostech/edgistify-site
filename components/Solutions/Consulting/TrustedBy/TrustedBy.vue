<template>
  <v-container fluid class="TrustedBy">
    <h1> Trusted By </h1>
    <v-row no-gutters class="icons-container pt-6">
      <v-col class="icon pr-md-12 pr-6 pb-6" sm="6" md="2" cols="4">
        <v-img src="/Brands/1.png" class="img" contain />
      </v-col>

      <v-col class="icon px-md-6 px-3 pb-6"  sm="6" md="2" cols="4">
        <v-img src="/Brands/2.png" class="img" contain />
      </v-col>

      <v-col class="icon px-md-6 pl-6 pb-6"  sm="6" md="2" cols="4">
        <v-img src="/Brands/3.png" class="img" contain />
      </v-col>

      <v-col class="icon px-md-6 pr-6 pb-6"  sm="6" md="2" cols="4">
        <v-img src="/Brands/4.png" class="img" contain />
      </v-col>

      <v-col class="icon px-md-6 px-3 pb-6"  sm="6" md="2" cols="4">
        <v-img src="/Brands/6.png" class="img" contain />
      </v-col>

      <v-col class="icon pl-md-12 pl-6 pb-6"  sm="6" md="2" cols="4">
        <v-img src="/Brands/7.png" class="img" contain />
      </v-col>
    </v-row>
  </v-container>
</template>


 
<style lang="scss" scoped>
.TrustedBy {
  h1 {
    font-size: 42px;
  }

  background-color: white;
  height: auto;
  font-size: 2rem;
  font-family: "Noto Serif";
  position: relative;
  line-height: 69.1px;
  color: #0c0c0c;
  padding: 3% 6%;

  .icons-container {
    .icons {
      display: flex;
      height: auto;
      position: relative;
      overflow: hidden;
    }
  }
}

@media (max-width: 850px) {

  .TrustedBy {
    font-size: 30px !important;
  }
  .icons-container {
    .icons {
      display: block !important;
      position: relative !important;
      overflow: unset !important;
    }
  }
}
</style>
