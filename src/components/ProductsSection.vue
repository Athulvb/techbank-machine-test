<script setup lang="ts"></script>

<template>
  <section class="products-section">
    <div class="section-container">
      <div class="section-title">
        <span class="section-subtitle">Innovative</span>
        <h2 class="section-heading">PRODUCTS</h2>
      </div>
      <div class="products-grid">
        <div class="product-card">
          <div class="product-image">
            <img class="product-photo" src="/img/dwallet_product.png" alt="DWALLET" />
            <img class="product-badge" src="/img/dwallet_icon.png" alt="DWALLET icon" />
          </div>
          <div class="product-header">
            <h3 class="product-title">DWALLET</h3>
            <button class="product-view-btn">
              View
              <svg
                width="16"
                height="16"
                viewBox="0 0 16 16"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M3.5 12.5L12.5 3.5M12.5 3.5H5.5M12.5 3.5V10.5"
                  stroke="white"
                  stroke-width="1.6"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </button>
          </div>
          <p class="product-description">
            A secure, intuitive crypto wallet for managing your digital assets.
          </p>
        </div>

        <div class="product-card">
          <div class="product-image">
            <img class="product-photo" src="/img/dbank_product.png" alt="DBANK" />
            <img class="product-badge" src="/img/dbank_icon.png" alt="DBANK icon" />
          </div>
          <div class="product-header">
            <h3 class="product-title">DBANK</h3>
            <button class="product-view-btn">
              View
              <svg
                width="16"
                height="16"
                viewBox="0 0 16 16"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M3.5 12.5L12.5 3.5M12.5 3.5H5.5M12.5 3.5V10.5"
                  stroke="white"
                  stroke-width="1.6"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </button>
          </div>
          <p class="product-description">
            A secure staking platform for earning rewards on your digital assets.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.products-section {
  background-color: #000000;
}

.section-container {
  max-width: 1400px;
  margin: 0 auto;
  padding: 6rem 3rem;
}

.section-title {
  text-align: center;
  margin-bottom: 3rem;
}

.section-subtitle {
  display: block;
  font-size: 1.125rem;
  font-weight: 400;
  color: #b38aff;
  letter-spacing: 0.02em;
  margin-bottom: 0.25rem;
}

.section-heading {
  font-size: 32px;
  font-family: 'NYXERIN', sans-serif;
  font-weight: 400;
  color: #ffffff;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  margin-top: 10px;
}

.products-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 3rem;
  max-width: 1200px;
  margin: 0 auto;
}

.product-card {
  background-color: #000000;
  border: 1px solid rgba(255, 255, 255, 0.15);
  border-radius: 18px;
  padding: 1rem 1rem 1.5rem 1rem;
  display: flex;
  flex-direction: column;
  gap: 1rem;
  transition:
    transform 0.3s,
    box-shadow 0.3s;
}

.product-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 40px rgba(139, 92, 246, 0.2);
}

.product-image {
  width: 100%;
  height: 300px;
  border-radius: 14px;
  overflow: hidden;
  position: relative;
  background: linear-gradient(135deg, rgba(139, 92, 246, 0.1) 0%, rgba(59, 130, 246, 0.1) 100%);
}

.product-photo {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.product-badge {
  position: absolute;
  bottom: -5%;
  left: 12px;
  transform: translateY(-50%);
  width: 50px;
  height: 50px;
}

.product-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.product-title {
  font-size: 28px;
  font-family: 'NYXERIN', sans-serif;
  font-weight: 400;
  color: #ffffff;
  text-transform: uppercase;
}

.product-description {
  font-size: 1rem;
  line-height: 1.6;
  color: #c0c0c0;
  opacity: 0.8;
  max-width: 400px;
}

.product-view-btn {
  background: linear-gradient(90deg, #330694 0%, #8500a6 100%);
  border: none;
  color: #ffffff;
  padding: 12px 36px;
  font-size: 1rem;
  font-weight: 500;
  cursor: pointer;
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  border-radius: 9999px;
  box-shadow: inset 0 0 0 1px rgba(255, 255, 255, 0.2);
  width: auto;
  transition: all 0.3s;
}

.product-view-btn:hover {
  transform: translateX(3px);
}

@media (max-width: 1200px) {
  .section-heading {
    font-size: 2.5rem;
  }

  .products-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 768px) {
  .section-container {
    padding: 4rem 2rem;
  }
}
</style>
