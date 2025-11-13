<script setup lang="ts"></script>

<template>
  <section class="brands-section">
    <div class="section-container">
      <div class="section-title">
        <span class="section-subtitle">From One Root, Many Branches</span>
        <h2 class="section-heading">OUR CONNECTED BRANDS</h2>
      </div>
      <div class="brands-grid">
        <div class="brand-card">
          <h3 class="brand-card-title">BLUE TIGERS</h3>
          <p class="brand-card-description">Fueling the Future of Film, Sports, and Technology.</p>
          <div class="brand-socials">
            <!-- LinkedIn -->
            <a href="#" target="_blank" aria-label="LinkedIn" class="brand-social-btn">
              <img src="/img/LinkedinLogo.png" alt="LinkedIn" style="width: 28px; height: 28px" />
            </a>
            <!-- Instagram -->
            <a href="#" target="_blank" aria-label="Instagram" class="brand-social-btn">
              <img src="/img/InstagramLogo.png" alt="Instagram" style="width: 28px; height: 28px" />
            </a>
            <!-- X -->
            <a href="#" target="_blank" aria-label="X" class="brand-social-btn">
              <img src="/img/XLogo.png" alt="X" style="width: 28px; height: 28px" />
            </a>
            <!-- YouTube -->
            <a href="#" target="_blank" aria-label="YouTube" class="brand-social-btn">
              <img src="/img/YoutubeLogo.png" alt="YouTube" style="width: 28px; height: 28px" />
            </a>
          </div>
          <img class="brand-card-image" src="/img/2.png" alt="Blue Tigers" />
        </div>
        <div class="brand-card">
          <h3 class="brand-card-title">KOCHI BLUE TIGERS</h3>
          <p class="brand-card-description">
            A dynamic cricket team redefining the game with passion and power.
          </p>
          <div class="brand-socials">
            <!-- Website -->
            <a href="#" target="_blank" aria-label="Website" class="brand-social-btn">
              <img src="/img/WorldLogo.png" alt="Website" style="width: 28px; height: 28px" />
            </a>
            <!-- LinkedIn -->
            <a href="#" target="_blank" aria-label="LinkedIn" class="brand-social-btn">
              <img src="/img/LinkedinLogo.png" alt="LinkedIn" style="width: 28px; height: 28px" />
            </a>
            <!-- Instagram -->
            <a href="#" target="_blank" aria-label="Instagram" class="brand-social-btn">
              <img src="/img/InstagramLogo.png" alt="Instagram" style="width: 28px; height: 28px" />
            </a>
            <!-- X -->
            <a href="#" target="_blank" aria-label="X" class="brand-social-btn">
              <img src="/img/XLogo.png" alt="X" style="width: 28px; height: 28px" />
            </a>
            <!-- YouTube -->
            <a href="#" target="_blank" aria-label="YouTube" class="brand-social-btn">
              <img src="/img/YoutubeLogo.png" alt="YouTube" style="width: 28px; height: 28px" />
            </a>
          </div>
          <img class="brand-card-image" src="/img/1.png" alt="Kochi Blue Tigers" />
        </div>
        <div class="brand-card">
          <h3 class="brand-card-title">BLUE TIGERS LONDON</h3>
          <p class="brand-card-description">
            A creative production house bringing bold stories to life.
          </p>
          <div class="brand-socials">
            <!-- LinkedIn -->
            <a href="#" target="_blank" aria-label="LinkedIn" class="brand-social-btn">
              <img src="/img/LinkedinLogo.png" alt="LinkedIn" style="width: 28px; height: 28px" />
            </a>
            <!-- Instagram -->
            <a href="#" target="_blank" aria-label="Instagram" class="brand-social-btn">
              <img src="/img/InstagramLogo.png" alt="Instagram" style="width: 28px; height: 28px" />
            </a>
            <!-- X -->
            <a href="#" target="_blank" aria-label="X" class="brand-social-btn">
              <img src="/img/XLogo.png" alt="X" style="width: 28px; height: 28px" />
            </a>
            <!-- YouTube -->
            <a href="#" target="_blank" aria-label="YouTube" class="brand-social-btn">
              <img src="/img/YoutubeLogo.png" alt="YouTube" style="width: 28px; height: 28px" />
            </a>
          </div>
          <img class="brand-card-image" src="/img/3.png" alt="Blue Tigers London" />
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.brands-section {
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
  font-size: 2.2rem;
  font-family: 'NYXERIN', sans-serif;
  font-weight: 400;
  color: #ffffff;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  margin-top: 10px;
}

.brands-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2.5rem;
  max-width: 1400px;
  margin: 0 auto;
}

.brand-card {
  /* border: linear-gradient(110deg, rgba(13, 5, 36, 0.91) 42%, rgba(35, 36, 38, 0.91) 100%); */
  position: relative;
  z-index: 1;
}
.brand-card::before {
  content: '';
  position: absolute;
  inset: 0;
  padding: 2px; /* border thickness */
  border-radius: 27px;
  background: linear-gradient(110deg, #bb83ff, #b1b1b1, #313131);
  -webkit-mask:
    linear-gradient(#fff 0 0) content-box,
    linear-gradient(#fff 0 0);
  -webkit-mask-composite: xor;
  mask-composite: exclude;
  z-index: -1;
  pointer-events: none;
  /* Fix for full background cover */
  width: 100%;
  height: 100%;
}
.brand-card {
  background: #000; /* make sure background overlays the border gap */
  /* other styles continue here */
  border-radius: 27px;
  /* box-shadow: 0 7px 38px 0 rgba(90, 65, 174, 0.2); */
  padding: 2.5rem 1.8rem 2.2rem 1.8rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  min-height: 540px;
}
.brand-card-image {
  width: 88%;
  height: auto;
  margin-bottom: 2.3rem;
  object-fit: contain;
  margin-top: 1.2rem;
}
.brand-card-title {
  font-size: 24px;
  font-weight: 400;
  color: #fff;
  text-align: left;
  align-self: flex-start;
  margin-bottom: 0.42rem;
  margin-top: auto;
  text-transform: uppercase;
  letter-spacing: 0.01em;
}
.brand-card-description {
  font-size: 14px;
  text-align: left;
  align-self: flex-start;
  color: #c0c0c0;
  margin-bottom: 1.06rem;
}
.brand-socials {
  display: flex;
  justify-content: flex-start;
  align-items: center;
  gap: 1.3rem;
  width: 100%;
}
.brand-social-btn {
  display: flex;
  border-radius: 50%;
  background: transparent;
  padding: 0.33rem;
  transition: background 0.2s;
}
.brand-social-btn:hover {
  background: #161616;
}
@media (max-width: 1100px) {
  .brands-grid {
    grid-template-columns: 1fr;
    max-width: 100%;
    gap: 2.2rem;
  }
  .brand-card {
    min-height: 420px;
    padding: 2rem 1.5rem 2rem 1.5rem;
  }
}
@media (max-width: 768px) {
  .section-container {
    padding: 4rem 1.2rem;
  }
  .brand-card {
    padding: 1.25rem 0.5rem 1.35rem 0.5rem;
  }
  .brand-card-image {
    width: 93%;
    margin-bottom: 2rem;
  }
}
</style>
