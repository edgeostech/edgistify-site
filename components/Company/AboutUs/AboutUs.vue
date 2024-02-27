<template>
  <div class="company-aboutus">
    <div class="aboutus-wrapper" id="company-aboutus">
      <h1>About <span>Edgistify</span></h1>
      <p>
        We are an integrated supply chain solutions company dedicated to developing distinctive solutions for B2B and B2C
        companies by combining a consultative approach, operational excellence and cutting-edge technology. We have
        designed our service model using industry-leading practices and rigorous operational diligence that provide
        customized and optimized supply chain solutions.
      </p>
      <p>
        At Edgistify, we believe comprehending our clients' pain points is paramount in delivering impactful results. Our
        expertise lies in designing, implementing, and executing integrated supply chains. Our services span the first
        mile, middle mile, and last mile and are upheld by our reliable warehousing and logistics network.
      </p>
      <p>
        We are committed to creating a robust and efficient supply chain that offers unparalleled value to our
        stakeholders. We focus on delivering on the following key parameters: Visibility, Agility, Automation and
        Optimization.
      </p>
      <!-- <div class="btn_container">
        <v-btn class="btn">Hop Onboard</v-btn>
      </div> -->
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
.company-aboutus {
  width: 100%;
  height: 481px;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  background: #0d0d0d !important;

  .aboutus-wrapper {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    h1 {
      font-family: "Noto Serif";
      font-style: normal;
      font-weight: 400;
      font-size: 42px;
      line-height: 49px;
      color: #ffffff;
    }

     span {
          color: #00a699 !important;
        }
    p {
      font-size: 16px;
      font-family: "Outfit";
      font-weight: lighter;
      line-height: 20px;
      width: 50%;
      margin: 1rem;
      color: #ffffff;
    }
  }
}

@media screen and (max-width: 850px) {
  .company-aboutus {
    width: 100%;
    height: auto !important;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    background: #0d0d0d !important;

    .aboutus-wrapper {
      width: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 6%;

      h1 {
        width: 100% !important;
        font-size: 30px !important;
        text-align: center !important;
        margin-bottom: 1rem !important;

        span {
          color: #00a699 !important;
        }
      }

      p {
        font-size: 16px !important;
        // font-weight: normal !important;
        font-style: normal !important;

        line-height: 20px !important;
        width: 100% !important;
        margin: 0rem !important;
        margin-bottom: 2rem !important;
      }
    }
  }
}
</style>
