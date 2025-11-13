<template>
  <section class="blogs-section">
    <div class="section-container">
      <div class="section-title">
        <span class="section-subtitle">Techbank</span>
        <h2 class="section-heading">BLOGS</h2>
      </div>

      <div class="carousel">
        <button class="arrow left" @click="prevBlog">
          <img class="left-arrow" src="/img/Vectorleft.png" alt="left icon" />
        </button>

        <div class="cards-wrapper">
          <div
            class="cards-track"
            :style="{ transform: `translateX(-${currentBlogIndex * (100 / 3)}%)` }"
          >
            <div v-for="(blog, i) in blogs" :key="i" class="blog-card">
              <div class="image-container">
                <img :src="blog.image" :alt="blog.title" />
              </div>
              <div class="card-content">
                <h3>{{ blog.title }}</h3>
                <p>{{ blog.description }}</p>
              </div>
            </div>
          </div>
        </div>

        <button class="arrow right" @click="nextBlog">
          <img class="right-arrow" src="/img/Vectorright.png" alt="right icon" />
        </button>
      </div>

      <div class="dots">
        <button
          v-for="(blog, i) in blogs"
          :key="i"
          class="dot"
          :class="{ active: i === currentBlogIndex }"
          @click="currentBlogIndex = i"
        ></button>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const currentBlogIndex = ref(0)

const blogs = [
  {
    title: 'SMART AI CHATBOT',
    description: 'Enhance customer engagement with personalized, AI-driven interactions.',
    image: '/img/blog1.png',
  },
  {
    title: 'SMART AI CHATBOT',
    description: 'Enhance customer engagement with personalized, AI-driven interactions.',
    image: '/img/blog2.png',
  },
  {
    title: 'SMART AI CHATBOT',
    description: 'Enhance customer engagement with personalized, AI-driven interactions.',
    image: '/img/blog3.png',
  },
  {
    title: 'SMART AI CHATBOT',
    description: 'Enhance customer engagement with personalized, AI-driven interactions.',
    image: '/img/blog1.png',
  },
]

const nextBlog = () => {
  currentBlogIndex.value = (currentBlogIndex.value + 1) % blogs.length
}

const prevBlog = () => {
  currentBlogIndex.value = (currentBlogIndex.value - 1 + blogs.length) % blogs.length
}
</script>

<style scoped>
* {
  box-sizing: border-box;
}

.blogs-section {
  background: #000000;
  padding: 80px 0;
  color: #ffffff;
  overflow: hidden;
}

.section-container {
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 40px;
  text-align: center;
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

.carousel {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 30px;
  margin-bottom: 40px;
}

.arrow {
  border: none;
  background: transparent;
  color: #444444;
  cursor: pointer;
  transition: color 0.3s ease;
  padding: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}

.arrow:hover {
  color: #9a6aff;
}

.arrow svg {
  width: 28px;
  height: 28px;
}

.cards-wrapper {
  flex: 1;
  overflow: hidden;
  max-width: 1000px;
}

.cards-track {
  display: flex;
  transition: transform 0.5s ease;
  gap: 20px;
}

.blog-card {
  background: #1a1a1a;
  border-radius: 16px;
  overflow: hidden;
  flex: 0 0 calc(33.333% - 14px);
  display: flex;
  flex-direction: column;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.5);
}

.blog-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 48px rgba(154, 106, 255, 0.2);
}

.image-container {
  height: 240px;
  overflow: hidden;
  background: #111111;
}

.image-container img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

.card-content {
  padding: 24px;
  background: #2b2b2b;
  text-align: left;
  flex: 1;
  display: flex;
  flex-direction: column;
}

.card-content h3 {
  font-size: 16px;
  text-transform: uppercase;
  margin: 0 0 12px 0;
  font-weight: 400;
  letter-spacing: 0.05em;
  color: #ffffff;
}

.card-content p {
  font-size: 14px;
  opacity: 0.75;
  margin: 0;
  line-height: 1.6;
  color: #ffffff;
}

.dots {
  display: flex;
  justify-content: center;
  gap: 8px;
}

.dot {
  width: 8px;
  height: 8px;
  border-radius: 50%;
  border: none;
  background: rgba(255, 255, 255, 0.3);
  cursor: pointer;
  transition: all 0.3s ease;
  padding: 0;
}

.dot:hover {
  background: rgba(255, 255, 255, 0.5);
}

.dot.active {
  /* width: 24px; */
  border-radius: 4px;
  background: white;
}

@media (max-width: 1024px) {
  .blog-card {
    flex: 0 0 calc(50% - 10px);
  }

  .section-title {
    font-size: 36px;
  }
}

@media (max-width: 768px) {
  .blogs-section {
    padding: 40px 0;
  }

  .section-container {
    padding: 0 20px;
  }

  .blog-card {
    flex: 0 0 100%;
  }

  .carousel {
    gap: 15px;
  }

  .section-title {
    font-size: 28px;
    margin-bottom: 40px;
  }
}
</style>
