<script setup lang="ts"></script>

<template>
  <section class="hero-section">
    <div class="hero-container">
      <div class="hero-content">
        <div class="hero-top-info">
          <img src="/img/Group 1597883877.png" alt="TechBank Innovations" class="top-info-badge" />
          <p class="top-info-text">
            At TechBank, we’re pioneering the technologies of tomorrow. From blockchain to AI, we’re
            building the digital landscape of the future, today.
          </p>
        </div>

        <div class="hero-main">
          <div class="hero-visual">
            <div class="shield-bg"></div>
            <img
              src="/img/comp.gif"
              alt="Diamond Jellyfish Animation"
              class="jellyfish-animation"
            />
          </div>
          <h1 class="hero-title">
            ENGINEERING<br />
            <span class="title-line-2">THE<span class="plus-sign">+</span>FUTURE</span>
          </h1>
        </div>

        <div class="hero-bottom-info">
          <p class="bottom-info-text">
            Empowering Businesses, Enabling Growth<br />TechBank’s Products for Success
          </p>
          <button class="view-products-btn">
            View Products
            <span class="btn-icon">
              <svg
                width="16"
                height="16"
                viewBox="0 0 16 16"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M3.5 12.5L12.5 3.5M12.5 3.5H5.5M12.5 3.5V10.5"
                  stroke="#8500a6"
                  stroke-width="1.6"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </span>
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero-section {
  padding: 2rem 0 6rem;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 80vh;
}

.hero-container {
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 3rem;
  width: 100%;
}

.hero-content {
  background: url('/img/Hero_mask.png') no-repeat;
  background-size: contain;
  border: 2px solid #000000;
  border-radius: 20px;
  padding: 1rem 3rem;
  position: relative;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 851px;
}

.hero-top-info {
  align-self: flex-end;
  display: flex;
  align-items: center;
  gap: 1rem;
  max-width: 460px;
  /* text-align: right; */
  /* margin-bottom: 2rem; */
  z-index: 2;
}

.top-info-badge {
  width: 64px;
  height: 64px;
  border-radius: 50%;
  object-fit: cover;
}

.top-info-text {
  padding-top: 10px;
  color: #C0C0C0;;
  font-weight: 400;
  /* line-height: 1.6; */
}

.hero-main {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 2rem;
  width: 100%;
}

.hero-visual {
  position: relative;
  width: 100%;
  max-width: 600px;
  height: 400px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 2rem;
}

.shield-bg {
  position: absolute;
  width: 250px;
  height: 250px;
  top: 10%;
  /* left: 10%; */
  opacity: 0.4;
  z-index: 1;
  background: url('/img/shield.png') no-repeat center;
  background-size: contain;
}

.jellyfish-animation {
  position: relative;
  z-index: 2;
  width: 100%;
  height: 600px;
  top: 30%;
  object-fit: contain;
  max-width: 500px;
  transform: rotate(30deg);
  transform-origin: center;
}

.hero-title {
  font-family: 'NYXERIN', sans-serif;
  font-weight: 400;
  font-style: normal;
  font-size: 93.69px;
  line-height: 102px;
  color: #000000;
  letter-spacing: 0;
  text-transform: uppercase;
  text-align: center;
  position: relative;
  z-index: 3;
}

.title-line-2 {
  display: inline-block;
  position: relative;
  font-family: 'NYXERIN', sans-serif;
  font-weight: 400;
  font-style: normal;
  font-size: 93.69px;
  line-height: 102px;
  letter-spacing: 0;
  text-transform: uppercase;
  text-align: center;
}

.plus-sign {
  color: #ffffff;
  font-size: 2.5rem;
  vertical-align: middle;
  margin: 0 0.1em;
  display: inline-block;
  font-weight: 300;
  line-height: 1;
}

.hero-bottom-info {
  margin-top: auto;
  display: flex;
  align-items: center;
  gap: 2rem;
  z-index: 2;
}

.bottom-info-text {
  font-size: 0.95rem;
  line-height: 1.6;
  color: #1a1a1a;
  text-align: left;
}

.view-products-btn {
  position: relative;
  background: linear-gradient(90deg, #330694 0%, #8500a6 100%);
  border: none;
  color: #ffffff;
  padding: 10px 64px 10px 20px;
  font-size: 1rem;
  font-weight: 400;
  cursor: pointer;
  display: inline-flex;
  align-items: center;
  border-radius: 9999px;
  transition:
    transform 0.25s ease,
    box-shadow 0.25s ease;
}

/* .view-products-btn:hover {
  transform: translateY(-3px);
  box-shadow:
    0 14px 32px rgba(133, 0, 166, 0.4),
    0 0 0 10px rgba(86, 35, 233, 0.2);
} */

.btn-icon {
  position: absolute;
  right: 3px;
  top: 50%;
  transform: translateY(-50%);
  width: 36px;
  height: 36px;
  border-radius: 50%;
  border: 1.5px solid rgba(255, 255, 255, 0.8);
  display: inline-flex;
  align-items: center;
  justify-content: center;
  background: #ffffff;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.15);
}

.btn-icon svg {
  width: 14px;
  height: 14px;
}

@media (max-width: 1200px) {
  .hero-title {
    font-size: 3.5rem;
  }

  .plus-sign {
    font-size: 2.5rem;
  }

  .hero-content {
    min-height: 500px;
    padding: 2rem 2rem;
  }

  .hero-visual {
    height: 350px;
    max-width: 500px;
  }

  .hero-bottom-info {
    flex-direction: column;
    gap: 1.5rem;
    text-align: center;
  }

  .bottom-info-text {
    text-align: center;
  }
}

@media (max-width: 768px) {
  .hero-title {
    font-size: 2.5rem;
  }

  .plus-sign {
    font-size: 1.8rem;
  }

  .hero-content {
    min-height: 400px;
    padding: 2rem 1.5rem;
  }

  .hero-visual {
    height: 250px;
    max-width: 100%;
    margin-bottom: 1.5rem;
  }

  .hero-top-info {
    align-self: center;
    flex-direction: column;
    text-align: center;
    max-width: 260px;
  }

  .hero-bottom-info {
    align-items: center;
  }

  .shield-bg {
    width: 150px;
    height: 150px;
    top: 15%;
    left: 5%;
  }
}
</style>
