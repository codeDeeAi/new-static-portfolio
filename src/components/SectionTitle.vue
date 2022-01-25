<template>
  <div
    :id="sectionID"
    class="text-center cursor-pointer my-3 text-xl md:text-2xl font-semibold group"
  >
    <span class="text-green-400">{</span> {{ title }}
    <span class="text-green-400">}</span>

    <div class="w-4/6 group-hover:border group-hover:border-green-400 mx-auto"></div>
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
