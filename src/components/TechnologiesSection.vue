<script setup lang="ts">
const logos = [
  { src: '/img/Logo01.png', alt: 'Technology logo 01' },
  { src: '/img/Logo02.png', alt: 'Technology logo 02' },
  { src: '/img/Logo03.png', alt: 'Technology logo 03' },
  { src: '/img/Logo04.png', alt: 'Technology logo 04' },
  { src: '/img/Logo05.png', alt: 'Technology logo 05' },
  { src: '/img/Logo06.png', alt: 'Technology logo 06' },
]

function shuffleArray<T>(array: T[]): T[] {
  for (let i = array.length - 1; i > 0; i -= 1) {
    const j = Math.floor(Math.random() * (i + 1))
    const temp = array[i]!
    array[i] = array[j]!
    array[j] = temp
  }
  return array
}

const displayedLogos = shuffleArray([...logos, ...logos])
const scrollDuration = Math.max(14, displayedLogos.length * 1.6) // seconds, tweakable
const carouselItems = [...displayedLogos, ...displayedLogos] // ensure enough items for smooth loop in each row
</script>

<template>
  <section class="technologies-section">
    <div class="section-container">
      <h2 class="section-title">TECHNOLOGIES</h2>
      <div class="carousel" aria-hidden="false">
        <!-- Row 1 -->
        <div class="carousel-row" role="presentation">
          <div class="carousel-track" :style="{ '--duration': `${scrollDuration}s` }">
            <div
              v-for="(logo, index) in carouselItems"
              :key="`row1-${logo.src}-${index}`"
              class="tech-logo"
            >
              <img :src="logo.src" :alt="logo.alt" />
            </div>
          </div>
        </div>

        <!-- Row 2 (reversed direction for visual variety) -->
        <div class="carousel-row" role="presentation">
          <div
            class="carousel-track reverse"
            :style="{ '--duration': `${Math.max(12, scrollDuration * 1.05)}s` }"
          >
            <div
              v-for="(logo, index) in carouselItems"
              :key="`row2-${logo.src}-${index}`"
              class="tech-logo"
            >
              <img :src="logo.src" :alt="logo.alt" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.technologies-section {
  background-color: #000000;
}

.section-container {
  /* constrain width and center, use smaller side padding for small screens */
  /* max-width: 1200px;
  margin: 0 auto; */
  padding: 6rem 1.5rem;
}

.section-title {
  text-align: center;
  margin-bottom: 2rem;
  font-size: 32px;
  font-family: 'NYXERIN', sans-serif;
  font-weight: 400;
  color: #ffffff;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  margin-top: 10px;
}

.carousel {
  width: 100%;
}

.carousel-row {
  overflow: hidden;
  width: 100%;
  /* give rows some vertical spacing */
  padding: 0.5rem 0;
}

.carousel-track {
  display: flex;
  gap: 80px;
  align-items: center;
  flex-wrap: nowrap;
  white-space: nowrap;
  /* control speed via CSS variable set inline */
  animation: marquee linear infinite;
  animation-duration: var(--duration, 20s);
}

/* reverse direction for second row */
.carousel-track.reverse {
  animation-direction: reverse;
}

@keyframes marquee {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-50%);
  }
}

/* pause on hover for accessibility */
.carousel-row:hover .carousel-track {
  animation-play-state: paused;
}

.tech-logo {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0.5rem;
  transition:
    transform 0.25s ease,
    border-color 0.25s ease;
  will-change: transform;
  flex: 0 0 auto;
}

.tech-logo img {
  max-width: 200px;
  width: 100%;
  height: auto;
  filter: brightness(0) invert(1);
  opacity: 0.9;
  transition:
    opacity 0.3s ease,
    transform 0.25s ease;
}

.tech-logo:hover {
  transform: translateY(-6px);
  border-color: rgba(255, 255, 255, 0.25);
  /* pause animation while interacting */
}

.tech-logo:hover img {
  opacity: 1;
  transform: scale(1.03);
}

/* Large laptops / smaller desktops */
@media (max-width: 1200px) {
  .section-title {
    font-size: 28px;
  }

  .carousel-track {
    gap: 40px;
  }

  .tech-logo img {
    max-width: 120px;
  }
}

/* Tablets */
@media (max-width: 900px) {
  .section-container {
    padding: 4rem 1rem;
  }

  .section-title {
    font-size: 24px;
  }

  .carousel-track {
    gap: 40px;
  }

  .tech-logo img {
    max-width: 100px;
  }
}

/* Small tablets / large phones */
@media (max-width: 600px) {
  .section-container {
    padding: 3rem 0.75rem;
  }

  .section-title {
    font-size: 24px;
  }

  .carousel-track {
    gap: 40px;
  }

  .tech-logo img {
    max-width: 100px;
  }
}

/* Mobile */
@media (max-width: 400px) {
  .section-title {
    font-size: 18px;
  }

  .carousel-track {
    gap: 40px;
  }

  .tech-logo img {
    /* allow mobile logos to be a bit larger while keeping aspect */
    max-width: 140px;
  }
}
</style>
