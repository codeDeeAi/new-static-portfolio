<template>
  <div
    class="font-mono text-gray-200 w-screen h-screen overflow-y-auto bg-zinc-800"
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
