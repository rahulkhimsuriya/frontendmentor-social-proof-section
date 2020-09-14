<template>
  <div id="app">
    <hero-section></hero-section>

    <testimonial-section></testimonial-section>
  </div>
</template>

<script>
import HeroSection from '@/pages/HeroSection.vue';
import TestimonialSection from '@/pages/TestimonialSection.vue';

export default {
  name: 'App',

  components: {
    HeroSection,
    TestimonialSection
  }
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Spartan:wght@400;500;700&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: 'Spartan', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-size: 15px;
  font-weight: 400;
  background-image: url('./assets/images/bg-pattern-top-desktop.svg'),
    url('./assets/images/bg-pattern-bottom-desktop.svg');
  background-repeat: no-repeat;
  background-position: 0% 0%, 100% 0%;
  min-height: 100vh;
}

section {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 1rem;
}

@media screen and (max-width: 1020px) {
  section {
    flex-direction: column;
    grid-gap: 1rem;
  }
}
</style>
