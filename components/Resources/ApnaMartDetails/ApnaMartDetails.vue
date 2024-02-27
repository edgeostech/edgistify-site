<template>
   <div class="details-container">
      <div class="challenges-wrapper">
         <label class="challenges">Challenges</label>
         <ul>
            <li>Apna Mart was in search of a service provider with expertise in end-to-end retail operations for its
               aggressive expansion in Eastern states.</li>
            <li>Required supply chain designer for cost optimization and achievement of delivery TAT.</li>
            <li>Aimed at digitalizing the inventory and implement FEFO at the fulfillment centers.</li>
            <li>Introduce and execute hyperlocal/same-day delivery for its customers in the Eastern states.</li>
            <li>First, mid and last-mile delivery designing based on retail business volume (Business as usual, peak business
               and buying cycle).</li>
            <li>Converting traditional stores to organized digital outlets.</li>
         </ul>
      </div>
      <div class="requirement-wrapper">
         <label class="requirement">Requirement</label>
         <ul>
            <li>Strategic location of warehouse providing deliveries to multiple cities.</li>
            <li>Cost-effective and efficient manpower.</li>
            <li>Well-experienced trainers for setting up SOPs and standards in the operations.</li>
            <li>Deployment of manpower with proper retail-specific training.</li>
         </ul>
      </div>
      <div class="solution-wrapper">
         <label class="solution">Solution</label>
         <ul>
            <li>Designing, Planning and Selecting Warehouses based on business requirements.</li>
            <li>Scouting a strategic location for the warehouse to optimize the supply chain.</li>
            <li>Designing and Setting up of 18000 sq. ft. mother warehouse for ~5000+ SKUs</li>
            <li>Operational design and manpower placement to cater 24X7 and 363 days a year.</li>
            <li>Setting up routes with beat plan for the mid mile</li>
            <li>Hiring and training delivery team for the last mile.</li>
            <li>Setting up a field team for new customer onboarding and auditing of operational stores to ensure zero
               discrepancies in stock.</li>
         </ul>
      </div>
      <div class="numbers-wrapper">
         <label class="numbers">Numbers</label>
         <ul>
            <li>SKU - 1718</li>
            <li>Inbound Volume Monthly - 4145056</li>
            <li>Outbound Volume Monthly - 2500000</li>
            <li>Area (sq.ft.)- 18000</li>
            <li>Fulfillment- 98%</li>
            <li>% Return- 4%</li>
         </ul>
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
   .numbers-wrapper {
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
   }
}

@media screen and (max-width: 850px) {
   .details-container {

      .challenges-wrapper,
      .requirement-wrapper,
      .solution-wrapper,
      .numbers-wrapper {
         padding-bottom: 20% !important;

         label {
            font-size: 1.5rem !important;
            line-height: 2.063rem !important;
         }

         ul {
            padding-left: 1%;
            padding-right: 12% !important;

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
      }
   }
}
</style>