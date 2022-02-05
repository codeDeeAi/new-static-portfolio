<template>
  <div
    class="font-mono text-gray-300 w-screen h-screen overflow-y-auto bg-zinc-800"
  >
    <div class="w-5/6 mt-6 h-full mx-auto">
      <!-- Nav Bar -->
      <NavBar />
      <!-- Nav Bar Ends -->
      <!-- Hero Section -->
      <HeroSection />
      <!-- Hero Section Ends -->
      <!-- Introduction -->
      <IntroSection />
      <!-- Introduction Ends -->
    </div>
  </div>
</template>
<script>
import NavBar from "./components/NavBar.vue";
import HeroSection from "./components/Header.vue";
import IntroSection from "./components/IntroSection.vue";
export default {
  components: {
    NavBar,
    HeroSection,
    IntroSection,
  },
  data() {
    return {};
  },
};
</script>
<style>
/* Global Css Styles */
.overflow-auto::-webkit-scrollbar {
  /* Hide for chrome, safari and opera */
  display: none;
}
.overflow-auto {
  /* Hide for chrome, safari and opera */
  -webkit-scrollbar: none;
  /* Hide for Edge and Firefox */
  -ms-overflow-style: none;
}
</style>
