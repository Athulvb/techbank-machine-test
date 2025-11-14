<script setup lang="ts">
import ContactForm from '@/components/ContactForm.vue'
import TechBankFooter from '@/components/TechBankFooter.vue'
import TechBankHeader from '@/components/TechBankHeader.vue'
</script>

<template>
  <div class="contact-page">
    <TechBankHeader />
    <ContactForm />
    <TechBankFooter title="Relax, we get you and we’ve got you." />
  </div>
</template>

<style scoped>
.contact-page {
  background-color: #000000;
  color: #ffffff;
  min-height: 100vh;
}
</style>
