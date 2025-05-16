<script setup>
import Nav from './components/Nav.vue'
import Hero from './components/Hero.vue'
import Experience from './components/Experience.vue'
import SkillsBadges from './components/SkillsBadges.vue'
import Education from './components/Education.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="bg-white dark:bg-gray-900">
    <div class="container max-w-5xl px-4 mx-auto text-gray-900 bg-white dark:bg-gray-900 dark:text-white">  
      <Nav />
      <div class="scroll-mt-16" id="about">
        <Hero />
      </div>
      <div class="scroll-mt-14" id="experience">
        <Experience />
      </div>
      <div class="scroll-mt-16" id="education">
        <Education />
      </div>
      <div class="scroll-mt-24" id="skills">
        <SkillsBadges />
      </div>
      <div class="scroll-mt-16" id="contact">
        <Contact />
      </div>
      <Footer />
    </div>
  </div>
</template>


