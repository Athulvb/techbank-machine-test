<script setup lang="ts">
const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: 'smooth' })
}
</script>

<template>
  <footer class="footer">
    <img class="footer-bg-img" src="/img/Footer-image.png" alt="TechBank Footer Background" />
    <div class="footer-alignment">
      <div class="footer-container">
        <div class="footer-left">
          <div class="footer-logo-brand">
            <img src="/img/Logo.png" alt="TechBank Logo" class="footer-logo-img" />
          </div>
        </div>

        <div class="footer-right">
          <a href="mailto:hi@techbank.com" class="footer-email">hi@techbank.com</a>
        </div>
      </div>
      <div class="footer-middle">
        <div>
          <div class="footer-taglines">
            <span>ENGINEERING</span>
            <span>THE FUTURE</span>
          </div>
          <button class="contact-btn">CONTACT US</button>
        </div>
        <div class="footer-links">
          <div class="footer-col">
            <a href="#" class="active">Home</a>
            <a href="#">Products</a>
            <a href="#">Teams</a>
            <a href="#">Career</a>
            <a href="#">Blog</a>
          </div>
          <div class="footer-col footer-col-office">
            <span class="col-title">Offices</span>
            <a href="#">Infopark</a>
            <a href="#">Kochi - Kerala</a>
          </div>
        </div>
      </div>

      <!-- Bottom -->
      <div class="footer-bottom">
        <div class="social-icons">
          <a href="#"><img src="/img/LinkedinLogo.png" alt="LinkedIn" /></a>
          <a href="#"><img src="/img/InstagramLogo.png" alt="Instagram" /></a>
          <a href="#"><img src="/img/XLogo.png" alt="X" /></a>
          <a href="#"><img src="/img/YoutubeLogo.png" alt="YouTube" /></a>
        </div>
        <p>© 2025 Techbank</p>
        <div class="legal-links">
          <a href="#">Privacy Policy</a>
          <a href="#">Terms and Conditions</a>
        </div>
      </div>
    </div>

    <!-- Scroll to top -->
    <button class="scroll-top" @click="scrollToTop">
      <svg
        width="20"
        height="20"
        viewBox="0 0 20 20"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M10 15V5M10 5L5 10M10 5L15 10"
          stroke="white"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
        />
      </svg>
    </button>
  </footer>
</template>

<style scoped>
.footer {
  position: relative;
  background: #000;
  color: #fff;
  overflow: hidden;
  padding: 5rem 10rem 2rem;
  text-align: left;
}
.footer-bg-img {
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  width: 100%;
  height: auto;
  min-height: 320px;
  max-height: 38vw;
  object-fit: cover;
  pointer-events: none;
  z-index: 0;
  opacity: 1;
}
.footer::after {
  /* hide previous gradient overlay */
  display: none;
}

.footer-alignment {
  margin-bottom: 90px;
}
.footer-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  z-index: 2;
}

.footer-left {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 2.2rem;
  min-width: 300px;
  margin-top: 0.8rem;
}

.footer-logo-brand {
  display: flex;
  align-items: center;
  gap: 1.2rem;
  margin-bottom: 1.2rem;
}
.footer-logo-img {
  width: 200px;
  height: 50px;
}
.footer-brand-name {
  font-size: 2rem;
  font-weight: 400;
  letter-spacing: -0.5px;
}
.footer-taglines {
  font-family: 'NYXERIN', sans-serif;
  font-size: 32px;
  font-weight: 400;
  color: #ffffff;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  margin-top: 10px;
  margin-bottom: 20px;
}
.footer-taglines span {
  display: block;
}
.contact-btn {
  margin-bottom: 1.5rem;
  background: transparent;
  border: 1px solid #fff;
  border-radius: 50px;
  color: #fff;
  padding: 0.7rem 2.2rem;
  font-weight: 400;
  font-size: 1.05rem;
  text-transform: uppercase;
  transition: 0.3s;
  cursor: pointer;
}
.contact-btn:hover {
  background: #fff;
  color: #430072;
}

/* Socials */
.social-icons {
  display: flex;
  gap: 2rem;
  margin-left: 0;
  margin-bottom: 1rem;
}

.social-icons img {
  width: 32px;
  height: 32px;
  opacity: 0.8;
  transition: opacity 0.3s;
}

.social-icons img:hover {
  opacity: 1;
}

/* Middle Section */
.footer-links {
  display: flex;
  gap: 5rem;
  margin-top: 1.8rem;
}

.footer-col {
  display: flex;
  flex-direction: column;
  gap: 1.1rem;
}
.footer-col-office {
  margin-left: 2.5rem;
}

.footer-col a {
  color: #ddd;
  text-decoration: none;
  font-size: 1.16rem;
  transition: color 0.3s;
}

.footer-col a.active,
.footer-col a:hover {
  color: #fff;
  text-decoration: underline;
}

.col-title {
  font-weight: 400;
  font-size: 1.12rem;
  color: #fff;
  margin-bottom: 0.3rem;
}

/* Right Section */
.footer-right {
  min-width: 220px;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  margin-top: 0.1rem;
  gap: 1rem;
}

.footer-right a {
  color: #fff;
  text-decoration: none;
  font-size: 1.15rem;
  transition: color 0.3s;
}

.footer-right a:hover {
  color: #a855f7;
}
.footer-email {
  color: #fff;
  font-size: 1.15rem;
  text-decoration: none;
  font-weight: 500;
  margin-bottom: 0.2rem;
  transition: color 0.3s;
}
.footer-email:hover {
  color: #a855f7;
}

.footer-middle {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

/* Bottom Row */
.footer-bottom {
  margin-top: 2.7rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 2.5rem;
  position: relative;
  z-index: 2;
}

.footer-bottom p {
  color: #ccc;
  margin: 0;
}

.legal-links {
  display: flex;
  gap: 1.8rem;
}

.legal-links a {
  color: #ccc;
  text-decoration: none;
  font-size: 1rem;
  transition: color 0.3s;
}

.legal-links a:hover {
  color: #a855f7;
}

/* Scroll to Top */
.scroll-top {
  position: absolute;
  bottom: 2.8rem;
  right: 2.8rem;
  background: rgba(255, 255, 255, 0.08);
  border: 1px solid rgba(255, 255, 255, 0.3);
  border-radius: 50%;
  padding: 0.75rem;
  cursor: pointer;
  z-index: 5;
  transition: all 0.3s ease;
}

.scroll-top:hover {
  background: linear-gradient(135deg, #8b5cf6 0%, #3b82f6 100%);
  border-color: transparent;
}

.scroll-top svg {
  display: block;
}

/* Responsive */
@media (max-width: 1024px) {
  .footer-container {
    flex-direction: column;
    align-items: flex-start;
    gap: 2.5rem;
  }
  .footer-links {
    flex-direction: row;
    gap: 2rem;
    margin-top: 1.2rem;
  }
  .footer-right {
    align-self: flex-end;
  }
}

@media (max-width: 768px) {
  .footer {
    padding: 3rem 1.2rem;
  }
  .footer-container {
    flex-direction: column;
    align-items: flex-start;
    gap: 2.2rem;
  }
  .footer-links {
    flex-direction: column;
    gap: 1.2rem;
  }
  .footer-right {
    align-items: flex-start;
    min-width: unset;
    margin-top: 0.5rem;
  }
}
</style>
