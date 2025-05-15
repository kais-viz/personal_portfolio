<script setup>
import Nav from './components/Nav.vue'
import Hero from './components/Hero.vue'
import Experience from './components/Experience.vue'
import Skills from './components/Skills.vue'
import Education from './components/Education.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="bg-white dark:bg-gray-900">
    <div class="container max-w-5xl px-4 mx-auto text-gray-900 bg-white dark:bg-gray-900 dark:text-white">  
      <Nav />
      <Hero />
      <Experience />
      <Education />
      <Skills />
      <Contact />
      <Footer />
    </div>
  </div>
</template>


