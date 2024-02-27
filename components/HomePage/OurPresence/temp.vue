<template>
   <v-col class="options-container">
      <v-col class="option py-0">
         <span data-aos="fade-up" data-aos-once="true" data-aos-easing="ease-in" data-aos-duration="1000"
            v-on:mouseenter="activeLink(0)" v-on:mouseleave="unLink()"
            :class="{ 'active-link': activeLink === 0 }">ABC</span>
      </v-col>
      <v-col class="option py-0">
         <span data-aos="fade-up" data-aos-once="true" data-aos-easing="ease-in" data-aos-duration="1000"
            v-on:mouseenter="activeLink(1)" v-on:mouseleave="unLink()"
            :class="{ 'active-link': activeLink === 1 }">EFG</span>
      </v-col>
      <v-col class="option py-0">
         <span data-aos="fade-up" data-aos-once="true" data-aos-easing="ease-in" data-aos-duration="1100"
            v-on:mouseenter="activeLink(2)" v-on:mouseleave="unLink()" :class="{ 'active-link': activeLink === 2 }">4.5
            HIG</span>
      </v-col>
      <v-col class="option py-0">
         <span data-aos="fade-up" data-aos-once="true" data-aos-easing="ease-in" data-aos-duration="1200"
            v-on:mouseenter="activeLink(3)" v-on:mouseleave="unLink()" :class="{ 'active-link': activeLink === 3 }">Pan
            PQR</span>
      </v-col>
   </v-col>
</template>

<script setup>

</script>

<style lang="scss" scoped></style>