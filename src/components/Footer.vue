<template>
  <footer class="relative bg-gray-900 text-white pt-16 pb-8">
    <div class="container mx-auto px-4">
      <div class="flex flex-col md:flex-row justify-between items-center md:items-start mb-12">
        <div class="mb-8 md:mb-0 text-center md:text-left">
          <h2 class="text-3xl font-bold mb-2 tracking-wide text-white">Dara Devit</h2>
          <p class="text-gray-400 max-w-xs text-lg">
            Frontend Developer & UI/UX Designer
          </p>
          <div class="flex justify-center md:justify-start space-x-4 mt-6">
            <a href="#" class="social-icon text-gray-400 hover:text-white"><i class="fab fa-github text-2xl"></i></a>
            <a href="#" class="social-icon text-gray-400 hover:text-white"><i class="fab fa-linkedin text-2xl"></i></a>
            <a href="#" class="social-icon text-gray-400 hover:text-white"><i class="fab fa-twitter text-2xl"></i></a>
            <a href="#" class="social-icon text-gray-400 hover:text-white"><i class="fab fa-dribbble text-2xl"></i></a>
          </div>
        </div>

        <div class="grid grid-cols-2 gap-8 sm:grid-cols-3">
          <div class="col-span-1">
            <h3 class="text-lg font-semibold mb-4 text-white">Explore</h3>
            <ul class="space-y-2 text-gray-400">
              <li><a href="#" class="link">Home</a></li>
              <li><a href="#" class="link">Projects</a></li>
              <li><a href="#" class="link">About</a></li>
              <li><a href="#" class="link">Contact</a></li>
            </ul>
          </div>
          <div class="col-span-1">
            <h3 class="text-lg font-semibold mb-4 text-white">Projects</h3>
            <ul class="space-y-2 text-gray-400">
              <li><a href="#" class="link">Web Apps</a></li>
              <li><a href="#" class="link">Mobile Apps</a></li>
              <li><a href="#" class="link">UI Designs</a></li>
              <li><a href="#" class="link">Open Source</a></li>
            </ul>
          </div>
          <div class="col-span-1">
            <h3 class="text-lg font-semibold mb-4 text-white">Legal</h3>
            <ul class="space-y-2 text-gray-400">
              <li><a href="#" class="link">Privacy</a></li>
              <li><a href="#" class="link">Terms</a></li>
              <li><a href="#" class="link">Cookies</a></li>
            </ul>
          </div>
        </div>
      </div>

      <div class="border-t border-gray-700 pt-8 mt-8">
        <div class="max-w-md mx-auto text-center">
          <h3 class="text-xl font-semibold mb-3 text-white">Stay Updated</h3>
          <p class="text-gray-400 mb-6 px-4">
            Subscribe to my newsletter for the latest projects and insights.
          </p>
          <div class="flex w-full">
            <input
              v-model="email"
              type="email"
              placeholder="Your email"
              class="flex-grow px-4 py-3 rounded-l-lg bg-gray-800 text-white focus:outline-none focus:ring-2 focus:ring-[#689d6a] transition-all"
            />
            <button
              @click="subscribe"
              class="bg-[#689d6a] hover:bg-[#8ec07c] px-6 py-3 rounded-r-lg font-medium transition-all text-black"
            >
              Subscribe
            </button>
          </div>
        </div>
      </div>

      <div class="text-center text-gray-500 text-sm mt-8">
        <p>&copy; {{ currentYear }} Dara Devit. All rights reserved.</p>
        <p class="mt-1">
          Built with <i class="fas fa-heart text-red-500"></i> and Vue.js
        </p>
      </div>
    </div>
  </footer>
</template>

<script setup>
import { ref } from 'vue';

const email = ref('');
const currentYear = new Date().getFullYear();

const subscribe = () => {
  if (!email.value || !email.value.includes('@')) {
    alert('Please enter a valid email address.');
    return;
  }
  alert(`Subscribed with: ${email.value}`);
  email.value = ''; // Reset email input after subscription
};
</script>

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
  color: #a9b665;
}
/* .link {
  @apply text-gray-400 hover:text-white transition;
} */
</style>