<script setup lang="ts">
import { RouterLink, useRouter } from 'vue-router'

const router = useRouter()
const goToContact = () => {
  router.push({ name: 'contact' })
}
</script>

<template>
  <header class="techbank-header">
    <div class="header-container">
      <div class="logo-section">
        <img src="/img/Logo.png" alt="TechBank Logo" class="logo-image" />
      </div>

      <nav class="nav-menu">
        <RouterLink to="/" class="nav-item">Home</RouterLink>
        <RouterLink to="/products" class="nav-item">Products</RouterLink>
        <RouterLink to="/teams" class="nav-item">Teams</RouterLink>
        <RouterLink to="/career" class="nav-item">Career</RouterLink>
        <RouterLink to="/blog" class="nav-item">Blog</RouterLink>
      </nav>

      <button class="contact-btn" @click="goToContact">CONTACT US</button>
    </div>
  </header>
</template>

<style scoped>
.techbank-header {
  background-color: #000000;
  padding: 1.5rem 0;
  position: sticky;
  top: 0;
  z-index: 1000;
  width: 100%;
}

.header-container {
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 3rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 2rem;
}

.logo-section {
  display: flex;
  /* align-items: center; */
  /* gap: 0.75rem; */
  flex-shrink: 0;
  height: 33px;
  width: 129px;
}

.nav-menu {
  display: flex;
  gap: 2.5rem;
  align-items: center;
  flex: 1;
  justify-content: center;
}

.nav-item {
  color: #ffffff;
  text-decoration: none;
  font-size: 1rem;
  font-weight: 400;
  transition: color 0.3s;
  position: relative;
  white-space: nowrap;
}

.nav-item:hover {
  color: #a855f7;
}

.nav-item.router-link-active {
  color: #a855f7;
}

.contact-btn {
  background: transparent;
  border: 1px solid #ffffff;
  color: #ffffff;
  padding: 0.75rem 2rem;
  font-size: 0.9rem;
  font-weight: 400;
  cursor: pointer;
  transition: all 0.3s;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  border-radius: 56px;
  white-space: nowrap;
  flex-shrink: 0;
}

.contact-btn:hover {
  background: rgba(255, 255, 255, 0.1);
  border-color: #ffffff;
}

@media (max-width: 1024px) {
  .header-container {
    padding: 0 2rem;
  }

  .nav-menu {
    gap: 1.5rem;
  }

  .nav-item {
    font-size: 0.9rem;
  }
}

@media (max-width: 768px) {
  .nav-menu {
    display: none;
  }

  .header-container {
    padding: 0 1.5rem;
  }
}
</style>
