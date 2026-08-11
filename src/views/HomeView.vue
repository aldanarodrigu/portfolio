<script setup lang="ts">
import { onMounted } from 'vue'

import HeroSection from '@/components/HeroSection.vue'
import AboutSection from '@/components/AboutSection.vue'
import StackSection from '@/components/StackSection.vue'
import ProjectsSection from '@/components/ProjectSection.vue'
import ContactSection from '@/components/ContactSection.vue'
import AppFooter from '@/components/Appfooter.vue'

onMounted(() => {
  const sections = document.querySelectorAll('section')

  const observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add('is-visible')
          observer.unobserve(entry.target)
        }
      })
    },
    {
      threshold: 0.15,
    },
  )

  sections.forEach((section) => {
    section.classList.add('scroll-hidden')
    observer.observe(section)
  })
})
</script>

<template>
  <HeroSection />
  <AboutSection />
  <StackSection />
  <ProjectsSection />
  <ContactSection />
  <AppFooter />
</template>

<style>
html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
}

section.scroll-hidden {
  opacity: 0;
  transform: translateY(35px);
  transition:
    opacity 0.7s ease,
    transform 0.7s ease;
}

section.scroll-hidden.is-visible {
  opacity: 1;
  transform: translateY(0);
}

@media (prefers-reduced-motion: reduce) {
  html {
    scroll-behavior: auto;
  }

  section.scroll-hidden {
    opacity: 1;
    transform: none;
    transition: none;
  }
}
</style>
