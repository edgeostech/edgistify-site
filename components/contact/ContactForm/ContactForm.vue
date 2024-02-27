<template>
    <div class="contact-form">
        <div class="form-title">
            <h1>
                Make an impact that matters. Join Our Team!
            </h1>
        </div>
        <div class="form">
            <form class="contact-form-design"  @submit.prevent="handleSubmit">
            <div class="line_row"> 
              <div class="field_container">
                <label class="field_title">First Name *:</label>
                <input v-model="fname" type="text"  id="fname" class="name_field" required>
              </div>
              <div class="field_container">
                <label class="field_title">Last Name :</label>
                <input v-model="lname" type="text" id="lname" class="name_field">
              </div>
            </div>
            <div class="line_row"> 
              <div class="field_container">
                <label class="field_title">Email *:</label>
                <input v-model="email" type="email" id="email" class="name_field" required>
                <!-- id="email" -->
              </div>
              <div class="field_container">
                <label class="field_title">Mobile Number *:</label>
                <input v-model="mobile" type="text" id="mobile" class="name_field" required>
                <!-- id="mobile" -->
              </div>
            </div>
            <div class="line_row"> 
              <div class="field_container">
                <label class="field_title">Alternate Mobile</label>
                <input v-model="altmobile" type="text" id="altmobile" class="name_field">
                <!-- id="altmobile" -->
              </div>
              <div class="field_container">
                <label class="field_title">Company/Organization *:</label>
                <input v-model="company" type="text" id="company" class="name_field" required>
                <!-- id="company" -->
              </div>
            </div>
            <div class="line_row"> 
              <div class="field_container">
                <label class="field_title">Services Looking for*</label>
                <select v-model="services" id="services" class="name_field">
                  <!-- id="dropdown" -->
                  <option value="option1">Option 1</option>
                  <option value="option2">Option 2</option>
                  <option value="option3">Option 3</option>
                </select>
              </div>
              <div class="field_container">
                <label class="field_title">Additional Comment</label>
                <input v-model="content" type="text" id="content" class="name_field">
                <!-- id="comment" -->
              </div>
            </div>         
            <!-- <div class="line_row"> 

              <div class="field_container">
                <label class="field_title">Date:</label>
                <input v-model="date" type="date" id="date" class="name_field" > -->
                <!-- id="Date" -->
              <!-- </div>
              <div class="field_container">
                <label class="field_title">time:</label>
                <input v-model="time" type="time" id="time" class="name_field" > -->
                <!-- id="time" -->
              <!-- </div>
            </div> -->
            <div class="form-btn">
               <div class="btn-container">
                  <button type="submit" class="button primary">Submit</button>
               </div>
            </div>
          </form>
        </div>
        
    </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>
@media (max-width: 800px) {
  h1 {
    padding-left: 30px !important;
  }
  .contact-form-design {
    flex-wrap: wrap;
    padding: 0 !important;
    .line_row {
      display: block !important;
      margin: 0 20px !important;
      padding-top: 5px !important;
      width: 85% !important;
      .field_container {
        margin: 10px !important;

      }
    }
  }
}
.contact-form{
    width: 100%;
    height: 845px;
    display: flex;
    flex-direction: column;
    align-content: center;
    align-items: center;
    background-color: #0C0C0C;
    .form-title{
        display: flex;
        position: relative;
        padding-top: 5%;
        align-content: center;
        justify-content: center;
        h1 {
            font-family: 'Noto Serif';
            font-style: normal;
            font-weight: 500;
            font-size: 36px;
            line-height: 49px;
            color: #F3F3F3;
        }
    }
    .form{
        display: flex;
        width: 100%;
        align-items: center;
        justify-content: center;
        // padding: 0 0 0 21.8%;
        .contact-form-design{
            display: flex;
            width: 100%;
            flex-direction: column;
            color: #ffffff;
            padding: 0 22.8% 0 21.8%;
            .line_row {
                width: 100%;
                display: flex;
                position: relative;
                padding-top: 10%;
                gap: 20%;
                // gap: 5%;
                // align-items: center;
                // justify-content: center;
                .field_container{
                    display: flex;
                    flex-direction: column;
                    position: relative;
                    // gap: 15%;
                    width: 100%;
                    .field_title{
                        // width: 600px;
                        // height: 20px;
                        position: relative;
                        font-family: 'Outfit';
                        font-style: normal;
                        font-weight: 400;
                        font-size: 16px;
                        // width: 100%;
                        // line-height: 20px;
                    }
                    .name_field{
                    box-sizing: border-box;
                    color: #ffffff;
                    position: relative;
                    width: 100%;
                    height: 30px;
                    border-bottom: 1px solid #fff;
                    }
                }
                }
                .form-btn {
                    width: 100%;
                    display: flex;
                    align-content: center;
                    justify-content: center;
                    padding-top: 10%;
                    position: relative;
                    .btn-container {
                        display: flex;
                        width: 156px;
                        height: 44px;
                        position: relative;
                   .button {
                        width: 100%;
                        font-style: normal;
                        font-weight: 600;
                        line-height: 20px;
                        color: #ffffff;
                        background: #00A699;
                        border-radius: 44px;
                        font-family: 'Noto Serif';
                        font-size: 16px;
                        text-transform: unset !important;
                        }
                    }
                }

             }
    }
}
</style>

