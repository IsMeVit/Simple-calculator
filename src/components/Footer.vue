<template>
  <footer class="relative bg-gray-900 text-white pt-16 pb-8">
    <!-- Wave divider -->
    <div class="footer-wave">
      <svg
        data-name="Layer 1"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 1200 120"
        preserveAspectRatio="none"
      >
        <path
          d="M321.39,56.44c58-10.79,114.16-30.13,172-41.86,
             82.39-16.72,168.19-17.73,250.45-.39,
             C823.78,31,906.67,72,985.66,92.83,
             c70.05,18.48,146.53,26.09,214.34,3V0H0V27.35A600.21,
             600.21,0,0,0,321.39,56.44Z"
          class="shape-fill"
        />
      </svg>
    </div>

    <div class="container mx-auto px-4">
      <div class="flex flex-col md:flex-row justify-between items-center md:items-start">
        <!-- Brand info -->
        <div class="mb-8 md:mb-0 text-center md:text-left">
          <h2 class="text-2xl font-bold mb-2">Ashtro William</h2>
          <p class="text-gray-400 max-w-xs">
            Frontend Developer & UI/UX Designer
          </p>

          <div class="flex justify-center md:justify-start space-x-4 mt-4">
            <a href="#" class="social-icon text-gray-400 hover:text-white">
              <i class="fab fa-github text-xl"></i>
            </a>
            <a href="#" class="social-icon text-gray-400 hover:text-white">
              <i class="fab fa-linkedin text-xl"></i>
            </a>
            <a href="#" class="social-icon text-gray-400 hover:text-white">
              <i class="fab fa-twitter text-xl"></i>
            </a>
            <a href="#" class="social-icon text-gray-400 hover:text-white">
              <i class="fab fa-dribbble text-xl"></i>
            </a>
          </div>
        </div>

        <!-- Navigation links -->
        <div class="grid grid-cols-2 gap-8 sm:grid-cols-3 mb-8 md:mb-0">
          <div>
            <h3 class="text-lg font-semibold mb-4">Explore</h3>
            <ul class="space-y-2">
              <li><a href="#" class="link">Home</a></li>
              <li><a href="#" class="link">Projects</a></li>
              <li><a href="#" class="link">About</a></li>
              <li><a href="#" class="link">Contact</a></li>
            </ul>
          </div>

          <div>
            <h3 class="text-lg font-semibold mb-4">Projects</h3>
            <ul class="space-y-2">
              <li><a href="#" class="link">Web Apps</a></li>
              <li><a href="#" class="link">Mobile Apps</a></li>
              <li><a href="#" class="link">UI Designs</a></li>
              <li><a href="#" class="link">Open Source</a></li>
            </ul>
          </div>

          <div>
            <h3 class="text-lg font-semibold mb-4">Legal</h3>
            <ul class="space-y-2">
              <li><a href="#" class="link">Privacy</a></li>
              <li><a href="#" class="link">Terms</a></li>
              <li><a href="#" class="link">Cookies</a></li>
            </ul>
          </div>
        </div>
      </div>

      <!-- Newsletter -->
      <div class="mt-12 mb-8 border-t border-gray-800 pt-8">
        <div class="max-w-md mx-auto text-center">
          <h3 class="text-xl font-semibold mb-2">Stay Updated</h3>
          <!-- <p class="text-gray-400 mb-4">
            Subscribe to my newsletter for the latest projects and insights.
          </p> -->
          <!-- <div class="flex">
            <input
              v-model="email"
              type="email"
              placeholder="Your email"
              class="flex-grow px-4 py-2 rounded-l-lg bg-gray-800 text-white focus:outline-none focus:ring-2 focus:ring-purple-600"
            />
            <button
              @click="subscribe"
              class="bg-purple-600 hover:bg-purple-700 px-6 py-2 rounded-r-lg font-medium transition"
            >
              Subscribe
            </button>
          </div> -->
        </div>
      </div>

      <!-- Copyright -->
      <div class="text-center text-gray-500 text-sm">
        <p>&copy; <span id="year">2025</span> Ashtro William. All rights reserved.</p>
        <p class="mt-1">
          Built with <i class="fas fa-heart text-red-500"></i> and Vue.js
        </p>
      </div>
    </div>
  </footer>
</template>

<!-- <script>
  document.querySelector('#year').innerText = new Date().getFullYear();
</script> -->

<!-- <script setup>
import { ref } from 'vue'

const email = ref('')

const subscribe = () => {
  if (!email.value) {
    alert('Please enter your email.')
    return
  }
  alert(`Subscribed with: ${email.value}`)
  email.value = ''
}
</script> -->

<style scoped>
.footer-wave {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  overflow: hidden;
  line-height: 0;
  transform: rotate(180deg);
}

.footer-wave svg {
  position: relative;
  display: block;
  width: calc(100% + 1.3px);
  height: 50px;
}

.footer-wave .shape-fill {
  fill: #ffffff;
}

.social-icon {
  transition: all 0.3s ease;
}

.social-icon:hover {
  transform: translateY(-3px);
}

/* .link {
  @apply text-gray-400 hover:text-white transition;
} */
</style>
