<script setup lang="ts">
import { RouterLink, useRouter } from 'vue-router'
import { ref } from 'vue'

const router = useRouter()
const isOpen = ref(false)
const goToContact = () => {
  router.push({ name: 'contact' })
  isOpen.value = false
}
const toggleMenu = () => {
  isOpen.value = !isOpen.value
}
</script>

<template>
  <header class="techbank-header">
    <div class="header-container">
      <div class="logo-section">
        <img src="/img/Logo.png" alt="TechBank Logo" class="logo-image" />
      </div>

      <!-- mobile menu button -->
      <button class="mobile-menu-btn" @click="toggleMenu" aria-label="Toggle menu" type="button">
        <span :class="['hamburger', { open: isOpen }]" aria-hidden="true"></span>
      </button>

      <nav class="nav-menu">
        <RouterLink to="/" class="nav-item">Home</RouterLink>
        <RouterLink to="/products" class="nav-item">Products</RouterLink>
        <RouterLink to="/teams" class="nav-item">Teams</RouterLink>
        <RouterLink to="/career" class="nav-item">Career</RouterLink>
        <RouterLink to="/blog" class="nav-item">Blog</RouterLink>
      </nav>

      <button class="contact-btn" @click="goToContact">CONTACT US</button>

      <!-- mobile drawer -->
      <div class="mobile-drawer" v-if="isOpen" @keydown.esc="isOpen = false">
        <nav class="mobile-nav">
          <RouterLink to="/" class="mobile-nav-item" @click="isOpen = false">Home</RouterLink>
          <RouterLink to="/products" class="mobile-nav-item" @click="isOpen = false"
            >Products</RouterLink
          >
          <RouterLink to="/teams" class="mobile-nav-item" @click="isOpen = false">Teams</RouterLink>
          <RouterLink to="/career" class="mobile-nav-item" @click="isOpen = false"
            >Career</RouterLink
          >
          <RouterLink to="/blog" class="mobile-nav-item" @click="isOpen = false">Blog</RouterLink>
        </nav>
        <button class="contact-btn mobile-contact" @click="goToContact">CONTACT US</button>
      </div>
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

/* mobile menu button */
.mobile-menu-btn {
  display: none;
  background: transparent;
  border: none;
  width: 44px;
  height: 44px;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  padding: 0;
}

.hamburger {
  display: block;
  position: relative;
  width: 22px;
  height: 2px;
  background: #fff;
  transition: transform 0.25s ease;
}
.hamburger::before,
.hamburger::after {
  content: '';
  position: absolute;
  left: 0;
  width: 22px;
  height: 2px;
  background: #fff;
  transition:
    transform 0.25s ease,
    top 0.25s ease,
    bottom 0.25s ease;
}
.hamburger::before {
  top: -7px;
}
.hamburger::after {
  bottom: -7px;
}
.hamburger.open {
  transform: rotate(45deg);
}
.hamburger.open::before {
  transform: rotate(90deg);
  top: 0;
}
.hamburger.open::after {
  transform: rotate(90deg);
  bottom: 0;
}

/* mobile drawer */
.mobile-drawer {
  position: absolute;
  top: calc(100% + 8px);
  right: 1.5rem;
  width: calc(100% - 3rem);
  max-width: 360px;
  background: linear-gradient(180deg, #0b0b0b 0%, #151515 100%);
  border: 1px solid rgba(255, 255, 255, 0.06);
  border-radius: 12px;
  padding: 1rem;
  display: flex;
  flex-direction: column;
  gap: 0.75rem;
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.6);
}

.mobile-nav {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}
.mobile-nav-item {
  color: #ffffff;
  text-decoration: none;
  padding: 0.6rem 0.5rem;
  border-radius: 8px;
}
.mobile-nav-item:hover {
  background: rgba(255, 255, 255, 0.03);
  color: #a855f7;
}

.mobile-contact {
  align-self: stretch;
  margin-top: 0.25rem;
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
  .mobile-menu-btn {
    display: flex;
  }
  .logo-section {
    width: 110px;
    height: 28px;
  }
  .contact-btn {
    display: none;
  }
}

@media (max-width: 480px) {
  .mobile-drawer {
    right: 1rem;
    left: 1rem;
    width: auto;
    max-width: none;
  }
}
</style>
