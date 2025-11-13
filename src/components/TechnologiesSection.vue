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
</script>

<template>
  <section class="technologies-section">
    <div class="section-container">
      <h2 class="section-title">TECHNOLOGIES</h2>
      <div class="technologies-grid">
        <div
          v-for="(logo, index) in displayedLogos"
          :key="`${logo.src}-${index}`"
          class="tech-logo"
        >
          <img :src="logo.src" :alt="logo.alt" />
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
  margin: 0 100px;
  padding: 6rem 3rem;
}

.section-title {
  text-align: center;
  margin-bottom: 3rem;
  font-size: 32px;
  font-family: 'NYXERIN', sans-serif;
  font-weight: 400;
  color: #ffffff;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  margin-top: 10px;
}

.technologies-grid {
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  gap: 2rem;
  /* max-width: 1000px; */
  margin: 0 auto;
}

.tech-logo img {
  max-width: 140px;
  width: 100%;
  height: auto;
  filter: brightness(0) invert(1);
  opacity: 0.9;
  transition: opacity 0.3s ease;
}

.tech-logo:hover {
  transform: translateY(-6px);
  border-color: rgba(255, 255, 255, 0.25);
}

.tech-logo:hover img {
  opacity: 1;
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

  .technologies-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}
</style>
