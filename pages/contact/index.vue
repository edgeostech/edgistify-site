<template>
  <div class="contact-container">
    <ContactUs />
    <ContactForm />
    <ContactOffice />
  </div>
</template>

<script>
import ContactForm from "../../components/contact/ContactForm/ContactForm.vue"
import ContactOffice from "../../components/contact/ContactOffice/ContactOffice.vue";
import ContactUs from "../../components/contact/ContactUs/ContactUs.vue"

export default {
  components: {
    ContactForm,
    ContactOffice,
    ContactUs,
  },
  setup () { },
};
</script>

<style lang="scss" scoped>
.contact_container {
  display: flex;
  width: 100%;
  height: auto;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
</style>