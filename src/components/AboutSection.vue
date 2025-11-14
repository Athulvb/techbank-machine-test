<script setup lang="ts"></script>

<template>
  <section class="about-section">
    <div class="section-container">
      <h2 class="section-title">ABOUT</h2>
      <p class="about-description">
        TechBank is a blockchain product company creating decentralized tools like TechBank, Dbank,
        and Dwallet to simplify digital finance. We empower users with secure, transparent, and
        user-friendly solutions for managing assets in the Web3 world.
      </p>
      <div class="metrics-grid">
        <div class="metric-item">
          <div class="metric-icon">4</div>
          <div class="metric-value">Products</div>
        </div>
        <div class="metric-item">
          <div class="metric-icon">2000+</div>
          <div class="metric-value">Active Users</div>
        </div>
        <div class="metric-item">
          <div class="metric-icon">1M+</div>
          <div class="metric-value">Downloads</div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-section {
  background-color: #000000;
}

.section-container {
  max-width: 1400px;
  margin: 0 auto;
  padding: 6rem 3rem;
}

.section-title {
  font-family: 'NYXERIN', sans-serif;
  font-weight: 400;
  font-style: normal;
  font-size: 32px;
  line-height: 54.77px;
  letter-spacing: 0;
  text-transform: uppercase;
  vertical-align: middle;
  text-align: center;
  color: #ffffff;
  margin-bottom: 3rem;
}

.about-description {
  font-size: 18px;
  line-height: 1.8;
  color: #ffffff;
  text-align: center;
  max-width: 900px;
  margin: 0 auto 4rem;
  color: #c0c0c0;
}

.metrics-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  /* gap: 3rem; */
  max-width: 700px;
  margin: 0 auto;
  align-items: center;
}

.metric-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 10px;
  padding: 0 2rem;
}

.metric-item:not(:last-child) {
  border-right: 1px solid rgba(255, 255, 255, 0.3);
}

.metric-icon {
  font-size: 32px;
  font-family: 'NYXERIN', sans-serif;
}

.metric-value {
  font-size: 16px;
  color: #c0c0c0;
}

@media (max-width: 1200px) {
  .section-title {
    font-size: 2.5rem;
  }
}

@media (max-width: 768px) {
  .section-container {
    padding: 4rem 2rem;
  }

  .section-title {
    font-size: 24px;
    margin-bottom: 0;
  }

  .about-description {
    font-size: 16px;
  }

  .metric-icon {
    font-size: 20px;
  }

  .metric-value {
    font-size: 14px;
  }

  .metric-item {
    border-right: none;
    padding: 0;
  }
}
</style>
