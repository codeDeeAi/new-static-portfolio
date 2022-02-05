<template>
  <div
    :id="sectionID"
    class="text-center cursor-pointer my-8 text-2xl md:text-3xl font-semibold group transition-all"
  >
    <span class="text-green-400 invisible group-hover:visible group-hover:animate-ping">{</span> 
    <span class="text-green-400 hover:text-gray-400 px-3">{{ title }}</span>
    <span class="text-green-400 invisible group-hover:visible group-hover:animate-ping">}</span>

    <!-- <div class="w-4/6 group-hover: group-hover:border-green-400 mx-auto"></div> -->
  </div>
</template>
<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    sectionID: {
      type: String,
      required: false,
    },
  },
  data() {
    return {};
  },
};
</script>
