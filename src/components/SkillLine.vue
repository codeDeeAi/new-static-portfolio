<template>
  <li class="flex items-start">
    <span class="mr-1">
      <svg
        class="w-5 h-5 mt-px text-deep-purple-accent-400"
        stroke="currentColor"
        viewBox="0 0 52 52"
      >
        <polygon
          stroke-width="4"
          stroke-linecap="round"
          stroke-linejoin="round"
          fill="none"
          points="29 13 14 29 25 29 23 39 38 23 27 23"
        ></polygon>
      </svg>
    </span>
    {{ message }}
  </li>
</template>
<script>
export default {
  props: {
    message: {
      type: String,
      required: true,
    },
  },
  data() {
    return {};
  },
};
</script>
