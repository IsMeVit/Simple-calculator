<script>
import Calculator from './components/Calculator.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Calculator,
    Footer,
  },
};
</script>

<template>
  <div class="flex flex-col min-h-screen overflow-x-hidden">
    <main class="flex-grow">
      <Calculator />
    </main>
    
    <Footer />
  </div>
</template>

<style>
/* You may not need this in Tailwind, but it's a good fallback */
body, html {
  margin: 0;
  padding: 0;
  height: 100%;
}
</style>