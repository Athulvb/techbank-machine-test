<script setup lang="ts">
import { ref } from 'vue'

const name = ref('')
const email = ref('')
const phone = ref('')
const message = ref('')

function submitForm() {
  console.log({ name: name.value, email: email.value, phone: phone.value, message: message.value })
  name.value = ''
  email.value = ''
  phone.value = ''
  message.value = ''
}
</script>

<template>
  <section class="contact-section">
    <div class="contact-container">
      <div class="mobile-form-header">
        <div class="kicker">BUILD THE FUTURE WITH US</div>
        <h2 class="title">CONTACT US</h2>
      </div>
      <div class="left-card">
        <div class="image-wrapper">
          <img src="/img/dwallet_product.png" alt="Dwallet product" />
          <div class="image-overlay">
            <h3>
              LET'S CONNECT AND
              <span>CREATE THE NEXT BIG</span>
              <span>THING IN TECH</span>
            </h3>
          </div>
        </div>
      </div>

      <div class="right-card">
        <div class="form-header">
          <div class="kicker">BUILD THE FUTURE WITH US</div>
          <h2 class="title">CONTACT US</h2>
        </div>

        <form class="contact-form" @submit.prevent="submitForm">
          <label class="field">
            <div class="field-label">Name *</div>
            <input type="text" v-model="name" placeholder="Enter Your Name" />
          </label>

          <label class="field">
            <div class="field-label">Email *</div>
            <input type="email" v-model="email" placeholder="Enter Email" />
          </label>

          <label class="field phone-field">
            <div class="field-label">Phone Number *</div>
            <div class="phone-row">
              <button type="button" class="country-code">🇮🇳 ▾</button>
              <input type="tel" v-model="phone" placeholder="Enter Your Phone Number" />
            </div>
          </label>

          <label class="field">
            <div class="field-label">Message</div>
            <textarea v-model="message" placeholder="Write your message"></textarea>
          </label>

          <div class="actions">
            <button class="send-btn" type="submit">
              <span>Send Message</span>
              <span class="send-circle">
                <svg
                  width="16"
                  height="16"
                  viewBox="0 0 16 16"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                  aria-hidden
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
        </form>
      </div>
    </div>
  </section>
</template>

<style scoped>
.contact-section {
  background: #000;
  padding: 4rem 2rem;
  color: #fff;
}

.contact-container {
  max-width: 1400px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2.5rem;
  align-items: stretch;
}

.mobile-form-header {
  display: none;
}

.left-card {
  display: flex;
  justify-content: center;
  align-items: stretch;
}

.image-wrapper {
  width: 100%;
  height: 100%;
  background: linear-gradient(180deg, rgba(255, 255, 255, 0.02), rgba(255, 255, 255, 0.01));
  border-radius: 28px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.6);
  position: relative;
  overflow: hidden;
  display: block;
}

.image-wrapper img {
  width: 100%;
  height: 100%;
  display: block;
  border-radius: 20px;
  object-fit: cover;
  object-position: center;
}

.image-overlay {
  position: absolute;
  top: 2rem;
  left: 2rem;
  right: 2rem;
  pointer-events: none;
}

.image-overlay h3 {
  font-family: 'NYXERIN', sans-serif;
  font-weight: 400;
  color: #000;
  font-size: 28px;
  line-height: 1.05;
  text-transform: uppercase;
  letter-spacing: 1px;
  text-align: center;
  text-shadow: 0 2px 10px rgba(0, 0, 0, 0.6);
}

.image-overlay h3 span {
  display: block;
  font-family: 'NYXERIN', sans-serif;
  font-weight: 400;
  -webkit-font-smoothing: antialiased;
}

.right-card {
  padding: 0 2rem;
}

.form-header .kicker {
  color: #b08aff;
  font-size: 12px;
  letter-spacing: 1px;
  margin-bottom: 0.6rem;
}

.form-header .title {
  font-family: 'NYXERIN', sans-serif;
  font-size: 48px;
  font-weight: 400;
  margin: 0 0 40px 0;
  color: #fff;
  letter-spacing: 2px;
}

.mobile-form-header .kicker {
  color: #b08aff;
  font-size: 12px;
  letter-spacing: 1px;
  margin-bottom: 0.6rem;
}

.mobile-form-header .title {
  font-family: 'NYXERIN', sans-serif;
  font-size: 32px;
  font-weight: 400;
  color: #fff;
  letter-spacing: 2px;
}

.contact-form {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.field {
  display: flex;
  flex-direction: column;
  gap: 0.6rem;
}

.field-label {
  font-size: 14px;
  color: #fff;
}

input[type='text'],
input[type='email'],
input[type='tel'],
textarea {
  background: #1a1a1a;
  border: 1px solid #474747;
  padding: 14px 16px;
  border-radius: 8px;
  color: #ddd;
  font-size: 16px;
  outline: none;
}

input::placeholder,
textarea::placeholder {
  color: #4e4e4e;
  letter-spacing: 0.4px;
}

textarea {
  min-height: 120px;
  resize: vertical;
}

.phone-field .phone-row {
  display: flex;
  gap: 0.6rem;
  align-items: center;
}

.phone-field .phone-row input {
  flex: 1 1 auto;
  min-width: 0;
}

.country-code {
  background: #1a1a1a;
  border: 1px solid #474747;
  color: #fff;
  padding: 15px 10px;
  border-radius: 8px;
  min-width: 64px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  flex: 0 0 auto;
}

.actions {
  margin-top: 0.5rem;
}

.send-btn {
  position: relative;
  display: inline-flex;
  align-items: center;
  gap: 12px;
  background: linear-gradient(90deg, #330694 0%, #8500a6 100%);
  color: #ffffff;
  padding: 14px 64px 14px 20px;
  border: none;
  border-radius: 9999px;
  font-size: 1rem;
  font-weight: 400;
  cursor: pointer;
  box-shadow: 0 14px 32px rgba(133, 0, 166, 0.18);
}

.send-btn span:first-child {
  z-index: 2;
}

.send-btn .send-circle {
  position: absolute;
  right: 6px;
  top: 50%;
  transform: translateY(-50%);
  background: #ffffff;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  color: #8500a6;
  border: 1.5px solid rgba(255, 255, 255, 0.85);
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.15);
  z-index: 3;
}

@media (max-width: 1000px) {
  .contact-container {
    grid-template-columns: 1fr;
    gap: 1.25rem;
  }

  .mobile-form-header {
    display: block;
    text-align: center;
    margin-bottom: 1rem;
  }

  .form-header {
    display: none;
  }

  .image-wrapper {
    height: 380px;
  }

  .image-overlay h3 {
    font-size: 22px;
  }

  .form-header .title {
    font-size: 36px;
    text-align: center;
  }

  .right-card {
    padding: 0 1rem;
  }

  .contact-form {
    gap: 0.75rem;
  }

  input[type='text'],
  input[type='email'],
  input[type='tel'],
  textarea {
    font-size: 15px;
    padding: 12px 14px;
  }

  .country-code {
    min-width: 56px;
    padding: 12px 8px;
    font-size: 14px;
  }

  .send-btn {
    width: 100%;
    justify-content: center;
    padding: 14px 20px;
    border-radius: 14px;
  }

  .send-btn .send-circle {
    right: 16px;
  }
}

@media (max-width: 480px) {
  .contact-section {
    padding: 2.5rem 1rem;
  }

  .mobile-form-header .kicker {
    color: #b08aff;
    font-size: 12px;
    letter-spacing: 1px;
    margin-bottom: 0.6rem;
  }

  .mobile-form-header .title {
    font-family: 'NYXERIN', sans-serif;
    font-size: 24px;
    font-weight: 400;
    color: #fff;
    letter-spacing: 2px;
  }

  .image-wrapper {
    height: 360px;
    border-radius: 20px;
  }

  .image-overlay h3 {
    font-size: 18px;
    top: 1rem;
  }

  .form-header .kicker {
    font-size: 11px;
  }

  .form-header .title {
    font-size: 28px;
    margin-bottom: 20px;
  }

  .country-code {
    min-width: 48px;
    padding: 10px 8px;
  }
  .actions {
    margin: 10px 60px;
  }

  .send-btn {
    border-radius: 38px;
    padding: 12px 18px;
    font-size: 15px;
  }

  .send-btn .send-circle {
    width: 36px;
    height: 36px;
    right: 4px;
  }

  .right-card {
    padding: 0 0.5rem;
  }
}
</style>
