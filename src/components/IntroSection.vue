<template>
  <div class="w-5/6 mx-auto my-6 md:my-12">
    <!-- About Me -->
    <div
    id="about-me"
      class="text-center border-b-2 border-green-400 cursor-pointer my-3 text-xl md:text-2xl font-semibold"
    >
      <span class="text-green-400">{</span> About Me
      <span class="text-green-400">}</span>
    </div>
    <article class="text-center">
      I am a graduate of Civil Engineering from Federal University, Oye-Ekiti,
      Nigeria and a Self Taught Software Developer whose interest in computers
      has led me to pursue a career in software development. I am a fast learner
      from an analytical background, a Tech Savvy with keen interest in solving
      problems, and providing fast, simple, easy to use and efficient solutions.
    </article>
    <!-- About Me Ends -->

    <!-- Skills  -->
    <div
      class="text-center border-b-2 border-green-400 cursor-pointer mt-6 my-3 text-xl md:text-2xl font-semibold"
    >
      <span class="text-green-400">{</span> Skills
      <span class="text-green-400">}</span>
    </div>

    <div class="grid gap-3 row-gap-3 md:grid-cols-2 lg:grid-cols-3">
      <ul class="space-y-3">
        <SkillLine
          v-for="(skill, index) in skills.set_one"
          :key="index"
          :message="skill"
        />
      </ul>
      <ul class="space-y-3">
        <SkillLine
          v-for="(skill, index) in skills.set_two"
          :key="index"
          :message="skill"
        />
      </ul>
      <ul class="space-y-3">
        <SkillLine
          v-for="(skill, index) in skills.set_three"
          :key="index"
          :message="skill"
        />
      </ul>
    </div>
    <!-- Skills End -->

    <!-- Tech & Tools -->
    <div
    id="tech-and-tools"
      class="text-center border-b-2 border-green-400 cursor-pointer mt-6 my-3 text-xl md:text-2xl font-semibold"
    >
      <span class="text-green-400">{</span> Tech & Tools
      <span class="text-green-400">}</span>
    </div>
    <div
      class="grid grid-cols-2 gap-5 row-gap-6 mb-10 sm:grid-cols-3 lg:grid-cols-6 my-4"
    >
      <div v-for="(tool, index) in tech_and_tools" :key="index" class="text-center group">
        <div
          class="flex items-center justify-center w-16 h-16 mx-auto mb-4 rounded bg-zinc-800 shadow-lg shadow-green-400 cursor-pointer"
        >
          <img
            :src="tool.link"
            :alt="tool.name"
            class="w-12 h-12 text-deep-purple-accent-400 sm:w-12 sm:h-12 group-hover:animate-pulse"
          />
        </div>
        <h6 class="mb-2 font-bold leading-5 uppercase">{{ tool.name }}</h6>
      </div>
    </div>
    <!-- Tech & Tools Ends -->
  </div>
  <div class="md:flex md:flex-row-reverse gap-6 w-5/6 mx-auto my-6 md:my-12">
    <!-- Section one -->
    <div class="p-5 bg-green-600 px-4 md:px-8 w-full md:w-1/2"></div>
    <!-- Section one Ends -->
    <!-- Section Two  -->
    <div class="p-5 px-4 md:px-8 space-y-2 w-full md:w-1/2">
      <div class="p-3 bg-zinc-700 group group-hover:shadow-xl cursor-pointer">
        <span class="font-bold text-lg group-hover:text-green-400">Design</span>
        <p class="text-xs md:text-sm">
          Lorem ipsum dolor sit amet, ritatis? Consequuntur nostrum omnis
          itaque?
        </p>
        <p class="mt-3 text-gray-400">Design</p>
      </div>
    </div>
    <!-- Section Two Ends -->
  </div>
</template>
<script>
import SkillLine from "./SkillLine.vue";
export default {
  components: {
    SkillLine,
  },
  data() {
    return {
      skills: {
        set_one: [
          "Business Analysis",
          "Problem solver and analytical thinker",
          "Proactive and learns fast ",
        ],
        set_two: [
          "Team Oriented",
          "Proficient with CSS Frameworks (Bootstrap, Materialize and Tailwind)",
          "Deep understanding of the internet and web",
          "Sufficient understanding of REST APIs and web security",
        ],
        set_three: [
          "Proficient with SQL Database management systems",
          "Proficient with HTML, CSS, JavaScript, Vue JS, Nuxt Js, Php, Laravel & SQL",
          "Proficient with Version Control (Git, GitHub, Bitbucket)",
          "Sufficient understanding of Jira",
        ],
      },
      tech_and_tools:[
          {
              link: "/svg/html5-svgrepo-com.svg",
              name: "HTML"
          },
          {
              link: "/svg/css3-svgrepo-com.svg",
              name: "CSS"
          },
          {
              link: "/svg/javascript-svgrepo-com.svg",
              name: "Javascript"
          },
          {
              link: "/svg/vue-9-logo-svgrepo-com.svg",
              name: "Vue Js"
          },
          {
              link: "/svg/nuxtjs-svgrepo-com.svg",
              name: "Nuxt Js"
          },
          {
              link: "/svg/php-svgrepo-com.svg",
              name: "Php"
          },
          {
              link: "/svg/laravel-svgrepo-com (1).svg",
              name: "Laravel"
          },
          {
              link: "/svg/sql-svgrepo-com.svg",
              name: "Sql"
          },
          {
              link: "/svg/git-svgrepo-com.svg",
              name: "Git"
          },
          {
              link: "/svg/github-svgrepo-com.svg",
              name: "Github"
          },
          {
              link: "/svg/bitbucket-svgrepo-com.svg",
              name: "Bitbucket"
          },
          {
              link: "/svg/jira-svgrepo-com.svg",
              name: "Jira"
          },
          {
              link: "/svg/vscode-svgrepo-com.svg",
              name: "Vscode"
          },
          {
              link: "/svg/bootstrap-fill-svgrepo-com.svg",
              name: "Bootstrap"
          },
          {
              link: "/svg/tailwind-svgrepo-com.svg",
              name: "Tailwind CSS"
          },
      ]
    };
  },
};
</script>
