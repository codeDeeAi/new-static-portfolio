<template>
  <!-- Mobile Menu -->
  <div
    class="fixed inset-0 overflow-hidden"
    aria-labelledby="slide-over-title"
    role="dialog"
    aria-modal="true"
    v-if="open_tray"
  >
    <div class="absolute inset-0 overflow-hidden">
      <!--
      Background overlay, show/hide based on slide-over state.

      Entering: "ease-in-out duration-500"
        From: "opacity-0"
        To: "opacity-100"
      Leaving: "ease-in-out duration-500"
        From: "opacity-100"
        To: "opacity-0"
    -->
      <div
        class="absolute inset-0 bg-zinc-500 bg-opacity-75 transition-opacity"
        aria-hidden="true"
      ></div>
      <div class="fixed inset-y-0 right-0 pl-10 max-w-full flex">
        <!--
        Slide-over panel, show/hide based on slide-over state.

        Entering: "transform transition ease-in-out duration-500 sm:duration-700"
          From: "translate-x-full"
          To: "translate-x-0"
        Leaving: "transform transition ease-in-out duration-500 sm:duration-700"
          From: "translate-x-0"
          To: "translate-x-full"
      -->
        <div class="relative w-screen max-w-md">
          <!--
          Close button, show/hide based on slide-over state.

          Entering: "ease-in-out duration-500"
            From: "opacity-0"
            To: "opacity-100"
          Leaving: "ease-in-out duration-500"
            From: "opacity-100"
            To: "opacity-0"
        -->
          <div
            class="absolute top-0 left-0 -ml-8 pt-4 pr-2 flex sm:-ml-10 sm:pr-4"
          >
            <button
              type="button"
              class="rounded-md text-gray-300 hover:text-white focus:outline-none focus:ring-2 focus:ring-white"
              @click="toggle_tray()"
            >
              <span class="sr-only">Close panel</span>
              <!-- Heroicon name: outline/x -->
              <svg
                class="h-6 w-6"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
                aria-hidden="true"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M6 18L18 6M6 6l12 12"
                />
              </svg>
            </button>
          </div>

          <div
            class="h-full flex flex-col py-6 bg-zinc-500 shadow-xl overflow-y-scroll"
          >
            <div class="px-4 sm:px-6">
              <h2
                class="text-lg font-medium text-gray-900"
                id="slide-over-title"
              >
                <span class="text-lg lg:text-2xl group"
                  ><a href="/" class="text-green-400 flex gap-2"
                    ><span class="visible">let name = {</span
                    ><span class="text-gray-200"
                      ><span class="font-semibold">Bada</span> Adeola</span
                    ><span class="visible">};</span></a
                  >
                </span>
              </h2>
            </div>
            <div class="mt-6 relative flex-1 px-4 sm:px-6 border-t-2">
              <!-- Replace with your content -->
              <div class="absolute inset-0 px-4 sm:px-6">
                <div class="h-full" aria-hidden="true">
                  <div class="py-3 text-lg" role="none">
                    <a
                      v-for="(nav, index) in navigation_list"
                      :key="index"
                      :href="nav.link"
                      @click="toggle_tray()"
                      class="px-4 py-2 group flex hover:gap-3"
                      role="menuitem"
                      tabindex="-1"
                      id="menu-item-0"
                    >
                      <span class="invisible text-green-400 group-hover:visible"
                        >{</span
                      ><span class="group-hover:text-green-400">{{
                        nav.name
                      }}</span>
                      <span class="invisible text-green-400 group-hover:visible"
                        >}</span
                      ></a
                    >
                  </div>
                </div>
              </div>
              <!-- /End replace -->
            </div>
            <!-- Copyright -->
            <p class="text-center">
              @ {{ new Date().getFullYear() }} Bada Adeola.
            </p>
            <!-- Copyright -->
          </div>
        </div>
      </div>
    </div>
  </div>
  <!-- Mobile Menu Ends -->
  <nav class="w-full flex justify-between">
    <span class="text-lg lg:text-2xl group"
      ><a href="/" class="group-hover:text-green-400 flex group-hover:gap-2"
        ><span class="invisible group-hover:visible">{</span
        ><span><span class="font-semibold">Bada</span> Adeola</span
        ><span class="invisible group-hover:visible">}</span></a
      >
    </span>
    <ul class="list-none hidden md:flex gap-2 text-sm mt-auto">
      <li
        v-for="(nav, index) in navigation_list"
        :key="index"
        class="group flex hover:gap-2"
      >
        <span class="invisible text-green-400 group-hover:visible">{</span
        ><a :href="nav.link" class="group-hover:text-green-400">{{
          nav.name
        }}</a
        ><span class="invisible text-green-400 group-hover:visible">}</span>
      </li>
    </ul>
    <ul class="list-none hidden md:flex gap-3 text-sm mt-auto">
      <li>
        <a href="https://github.com/codeDeeAi" target="_blank" class="hover:text-green-400">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="20"
            height="20"
            fill="currentColor"
            class="text-xl transition-colors duration-200"
            viewBox="0 0 1792 1792"
          >
            <path
              d="M896 128q209 0 385.5 103t279.5 279.5 103 385.5q0 251-146.5 451.5t-378.5 277.5q-27 5-40-7t-13-30q0-3 .5-76.5t.5-134.5q0-97-52-142 57-6 102.5-18t94-39 81-66.5 53-105 20.5-150.5q0-119-79-206 37-91-8-204-28-9-81 11t-92 44l-38 24q-93-26-192-26t-192 26q-16-11-42.5-27t-83.5-38.5-85-13.5q-45 113-8 204-79 87-79 206 0 85 20.5 150t52.5 105 80.5 67 94 39 102.5 18q-39 36-49 103-21 10-45 15t-57 5-65.5-21.5-55.5-62.5q-19-32-48.5-52t-49.5-24l-20-3q-21 0-29 4.5t-5 11.5 9 14 13 12l7 5q22 10 43.5 38t31.5 51l10 23q13 38 44 61.5t67 30 69.5 7 55.5-3.5l23-4q0 38 .5 88.5t.5 54.5q0 18-13 30t-40 7q-232-77-378.5-277.5t-146.5-451.5q0-209 103-385.5t279.5-279.5 385.5-103zm-477 1103q3-7-7-12-10-3-13 2-3 7 7 12 9 6 13-2zm31 34q7-5-2-16-10-9-16-3-7 5 2 16 10 10 16 3zm30 45q9-7 0-19-8-13-17-6-9 5 0 18t17 7zm42 42q8-8-4-19-12-12-20-3-9 8 4 19 12 12 20 3zm57 25q3-11-13-16-15-4-19 7t13 15q15 6 19-6zm63 5q0-13-17-11-16 0-16 11 0 13 17 11 16 0 16-11zm58-10q-2-11-18-9-16 3-14 15t18 8 14-14z"
            ></path></svg
        ></a>
      </li>
      <li>
        <a href="https://www.linkedin.com/in/adeola-bada-aiism-a51174124" target="_blank" class="hover:text-green-400"
          ><svg
            width="20"
            height="20"
            fill="currentColor"
            class="text-xl transition-colors duration-200"
            viewBox="0 0 1792 1792"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M477 625v991h-330v-991h330zm21-306q1 73-50.5 122t-135.5 49h-2q-82 0-132-49t-50-122q0-74 51.5-122.5t134.5-48.5 133 48.5 51 122.5zm1166 729v568h-329v-530q0-105-40.5-164.5t-126.5-59.5q-63 0-105.5 34.5t-63.5 85.5q-11 30-11 81v553h-329q2-399 2-647t-1-296l-1-48h329v144h-2q20-32 41-56t56.5-52 87-43.5 114.5-15.5q171 0 275 113.5t104 332.5z"
            ></path></svg
        ></a>
      </li>
    </ul>
    <span @click="toggle_tray()" class="md:hidden mt-auto"
      ><button type="button" class="flex hover:gap-2 group">
        <span class="invisible text-green-400 group-hover:visible">{</span
        ><a href="#!" class="group-hover:text-green-400">Menu</a
        ><span class="invisible text-green-400 group-hover:visible">}</span>
      </button></span
    >
  </nav>
</template>
<script>
export default {
  data() {
    return {
      open_tray: false,
      navigation_list: [
        { name: "About Me", link: "#about-me" },
        { name: "Tech & Tools", link: "#tech-and-tools" },
        { name: "Projects", link: "#projects" },
      ],
    };
  },
  methods: {
    toggle_tray() {
      if (this.open_tray) return (this.open_tray = false);
      return (this.open_tray = true);
    },
  },
};
</script>
