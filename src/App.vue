<script setup lang="ts">
import Navbar from "./components/Navbar.vue";
import About from "./components/About.vue";
import Carousel from "./components/Carousel/Carousel.vue"
import Projects from "./components/Projects.vue";
import Contact from "./components/Contact.vue";
import Footer from "./components/Footer.vue";
</script>

<template>
  <Navbar />
  <div class="mt-3 d-flex flex-column justify-content-md-center align-items-center">
    <About />
  </div>
  <Carousel />
  <Projects />
  <Contact />
  <Footer />
</template>

<style scoped></style>
