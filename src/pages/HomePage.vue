<script setup lang="ts">
import TechBankHeader from '../components/TechBankHeader.vue'
import HeroSection from '../components/HeroSection.vue'
import ProductsSection from '../components/ProductsSection.vue'
import TechnologiesSection from '../components/TechnologiesSection.vue'
import BlogsSection from '../components/BlogsSection.vue'
import TechBankFooter from '../components/TechBankFooter.vue'
import AboutSection from '@/components/AboutSection.vue'
import ConnectedBrandsSection from '@/components/ConnectedBrandsSection.vue'
</script>

<template>
  <div class="home-page">
    <TechBankHeader />
    <HeroSection />
    <AboutSection />
    <ProductsSection />
    <TechnologiesSection />
    <ConnectedBrandsSection />
    <BlogsSection />
    <TechBankFooter title = "Engineering The Future" />
  </div>
</template>

<style scoped>
.home-page {
  background-color: #000000;
  color: #ffffff;
  min-height: 100vh;
}
</style>
