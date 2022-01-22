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
      <!-- Floating Menu -->
      <FloatingMenu />
      <!-- Floating Menu Ends -->
    </div>
  </div>
</template>
<script>
import NavBar from "./components/NavBar.vue";
import HeroSection from "./components/Header.vue";
import FloatingMenu from "./components/FloatingMenu.vue";
export default {
  components: {
    NavBar,
    HeroSection,
    FloatingMenu,
  },
  data() {
    return {};
  },
};
</script>
