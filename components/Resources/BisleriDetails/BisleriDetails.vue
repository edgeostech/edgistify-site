<template>
   <div class="details-container">
      <div class="challenges-wrapper">
         <label class="challenges">Challenges</label>
         <ul>
            <li>Bisleri has introduced a D2C model by launching their official Application</li>
            <li>Although they are taking orders from the app, the delivery is a huge problem for them.</li>
            <li>As water is an essential resource, the delivery times have to be strictly adhered to. Since many cities
               like Noida, Bangalore struggle with the issues of drinking water, they are a huge market for a company like
               Bisleri.</li>
            <li>Bisleri is an established brand and it is comparatively trustworthy than the local purification plants.
            </li>
         </ul>
      </div>
      <div class="requirement-wrapper">
         <label class="requirement">Requirement</label>
         <p>Cost effective delivery and distribution for D2C orders followed by collection of empty cans.</p>
      </div>
      <div class="solution-wrapper">
         <label class="solution">Solution</label>
         <ul>
            <li>Planned distribution and collection of cans, keeping the weight and hygiene constraints in mind.</li>
            <li>Stored water nearby end customers ensuring timely delivery within defined morning and evening time slots.
            </li>
            <li>Used vehicles with optimum storage capacity, loading cans in a smarter and efficient manner.</li>
            <li>Cost effective option of shared storage spaces reducing the overall delivery cost.</li>
         </ul>
      </div>
      <div class="results-wrapper">
         <label class="results">Results</label>
         <p>Economical and timely D2C distribution for the brand.</p>
      </div>
   </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.details-container {
   display: flex;
   width: 100%;
   flex-direction: column;
   height: auto;
   background-color: #ffffff;
   padding: 6.5% 0 0 10%;

   .challenges-wrapper,
   .requirement-wrapper,
   .solution-wrapper,
   .results-wrapper {
      width: 100%;
      height: auto;
      display: flex;
      flex-direction: column;
      padding-bottom: 5%;

      label {
         width: 100%;
         height: auto;
         padding-bottom: 1.5%;
         font-family: 'Noto Serif';
         font-style: normal;
         font-weight: 300;
         font-size: 2.25rem;
         line-height: 3.063rem;
         color: #0C0C0C;
      }

      ul {
         padding-left: 1%;
         width: 85%;

         li {
            list-style: none;
            font-family: 'Outfit';
            font-style: normal;
            font-weight: 300;
            font-size: 1rem;
            line-height: 1.25rem;
            color: #313131;
         }

         li:before {
            content: "· ";
            font-size: 30px;
            vertical-align: middle;
            line-height: 24px;
         }
      }

      p {
         font-family: 'Outfit';
         font-style: normal;
         font-weight: 300;
         font-size: 1rem;
         line-height: 1.25rem;
         color: #313131;
      }
   }
}

@media screen and (max-width: 850px) {
   .details-container {

      .challenges-wrapper,
      .requirement-wrapper,
      .solution-wrapper,
      .results-wrapper {
         padding-bottom: 20% !important;

         label {
            font-size: 1.5rem !important;
            line-height: 2.063rem !important;
         }

         ul {
            padding-left: 1%;
            padding-right: 12% !important;
            width: 100% !important;


            li {
               font-size: 0.75rem !important;
               line-height: 0.938rem !important;
            }

            li:before {
               content: "· ";
               font-size: 24px !important;
               line-height: 0px !important;
            }
         }

         p {
            font-size: 0.75rem !important;
            line-height: 0.938rem !important;
            padding-right: 10% !important;
         }
      }
   }
}
</style>