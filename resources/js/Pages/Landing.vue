<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import Layout from '@/Layouts/Layout.vue';
import { Link } from '@inertiajs/vue3';
import '@fortawesome/fontawesome-free/css/all.css';
import '@fortawesome/fontawesome-free/js/all.js';

defineOptions({
    layout: Layout
});
</script>

<template>
  <AuthenticatedLayout>
    <div class="landing-container fade-in">
      <Sidebar></Sidebar>
      <div class="landing-content slide-up">
        <div class="about-me-card">
          <div class="about-me">
            <p class="text-lg leading-relaxed text-start">
              Hey, I'm Mathew Jerome Carillo, a third-year BSIT student at Mater Dei College. Alongside my studies, I enjoy honing my coding skills and exploring new technologies. In my free time, I indulge in playing online games, balancing my academic pursuits with some recreational fun. Thanks for visiting my page!
            </p>
            <div class="social-media-buttons">
          <a href="https://www.instagram.com" class="social-media-button">
            <i class="fab fa-instagram"></i>
          </a>
          <a href="https://twitter.com" class="social-media-button">
            <i class="fab fa-twitter"></i>
          </a>
          <a href="https://www.facebook.com" class="social-media-button">
            <i class="fab fa-facebook-f"></i>
          </a>
        </div>
          </div>
        </div>

      </div>
    </div>
  </AuthenticatedLayout>
</template>

<style scoped>
.landing-container {
  display: flex;
  height: 100vh;
  width: 100%;
  padding: 100px;
}

.landing-content {
  flex: 1;
  padding-left: 70px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.about-me-card {
  background: rgba(255, 255, 255, 0.3); /* Semi-transparent background */
  backdrop-filter: blur(10px); /* Blur effect */
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  margin-bottom: 20px;
}

.about-me {
  margin-bottom: 0rem;
}

.about-me h2 {
  font-size: 3rem;
}

p {
  font-size: 35px;
}

.social-media-buttons {
  display: flex;           /* Flexbox layout */
  justify-content: center; /* Center the icons horizontally */
  margin-top: 40px;
}

.social-media-button {
  font-size: 40px; /* Increased font size */
  margin-right: 40px; /* Increased margin for better spacing */
  color: #000;
  text-decoration: none;
  transition: color 0.3s ease;
}

.social-media-button:hover {
  color: #2e323a;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.fade-in {
  animation: fadeIn 1s ease-in-out;
}

@keyframes slideUp {
  from {
    transform: translateY(100%);
  }
  to {
    transform: translateY(0);
  }
}

.slide-up {
  animation: slideUp 1s ease-out;
}
</style>
