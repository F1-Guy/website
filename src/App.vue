<script lang="ts">
import Navbar from "./components/Navbar.vue";
import About from "./components/About.vue";
import Carousel, { CardType } from "./components/Carousel/Carousel.vue"
import Projects from "./components/Projects.vue";
import Contact from "./components/Contact.vue";
import Footer from "./components/Footer.vue";
import { defineComponent } from "vue";

const cards: CardType[] = [
  {
    title: "C#",
    imageName: "cs.svg"
  },
  {
    title: "Python",
    imageName: "py.svg"
  },
  {
    title: "JavaScript",
    imageName: "js.svg"
  },
  {
    title: "Vue.js",
    imageName: "vue.svg"
  },
  {
    title: "HTML",
    imageName: "html.svg"
  }
]

export default defineComponent({
  data() {
    return {
      cards: cards
    }
  },

  components: {
    Navbar,
    About,
    Carousel,
    Projects,
    Contact,
    Footer
  }
});


</script>

<template>
  <Navbar />
  <div class="mt-3 d-flex flex-column justify-content-md-center align-items-center">
    <About />
  </div>
  <Carousel :cards="cards" />
  <Projects />
  <Contact />
  <Footer />
</template>

<style scoped></style>
