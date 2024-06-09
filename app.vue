<template>
  <div class="home">
    <Navigation />
    <Hero />
  </div>
</template>

<script>
import Navigation from './components/NavigationComponent.vue';
import Hero from './components/hero'
export default {
  components: {
    Navigation,
    Hero
  }
}
</script>

<style scoped>
.home {
  background-color: var(--background-color);
  display: flex;
  flex-direction: column;
  align-items: center;
  height: 100vh;
  width: 100%;
}
</style>