<script setup>
import { RouterView } from 'vue-router';
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue'
</script>

<template>
  <div id="app" class="d-flex flex-column min-vh-100">
    <Navbar />
    <main class="container flex-grow-1 py-4">
      <RouterView />
    </main>
    <Footer />
  </div>
</template>

<style>
body {
  background-color: #0b1329 !important;
  color: #f8f9fa !important;
}
</style>