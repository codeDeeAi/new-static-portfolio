<template>
  <div class="w-5/6 mx-auto my-6 md:my-12 md:space-y-10 lg:space-y-20">
    <!-- About Me -->
    <section>
      <SectionTitle title="About Me" sectionID="about-me" />
      <article class="text-center">
        I am a Self Taught Software Developer whose interest in computers has
        led me to pursue a career in software development. I am a fast learner
        from an analytical background, a Tech Savvy with keen interest in
        solving problems, and providing fast, simple, efficient, and scalable
        web solutions.
      </article>
    </section>
    <!-- About Me Ends -->

    <!-- Skills  -->
    <section>
      <SectionTitle title="Skills" sectionID="" />

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
    </section>
    <!-- Skills End -->

    <!-- Tech & Tools -->
    <section>
      <SectionTitle title="Tech & Tools" sectionID="tech-and-tools" />
      <div
        class="grid grid-cols-2 gap-5 row-gap-6 mb-10 sm:grid-cols-3 lg:grid-cols-6 my-4"
      >
        <div
          v-for="(tool, index) in tech_and_tools"
          :key="index"
          class="text-center group"
        >
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
    </section>
    <!-- Tech & Tools Ends -->

    <!-- Experience -->
    <ExperienceTimeline />
    <!-- Experience Ends -->
  </div>
</template>
<script>
import SkillLine from "./SkillLine.vue";
import ExperienceTimeline from "./ExperienceTimeline.vue";
import SectionTitle from "./SectionTitle.vue";
export default {
  components: {
    SkillLine,
    ExperienceTimeline,
    SectionTitle,
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
      tech_and_tools: [
        {
          link: "/svg/html5-svgrepo-com.svg",
          name: "HTML",
        },
        {
          link: "/svg/css3-svgrepo-com.svg",
          name: "CSS",
        },
        {
          link: "/svg/javascript-svgrepo-com.svg",
          name: "Javascript",
        },
        {
          link: "/svg/vue-9-logo-svgrepo-com.svg",
          name: "Vue Js",
        },
        {
          link: "/svg/nuxtjs-svgrepo-com.svg",
          name: "Nuxt Js",
        },
        {
          link: "/svg/php-svgrepo-com.svg",
          name: "Php",
        },
        {
          link: "/svg/laravel-svgrepo-com (1).svg",
          name: "Laravel",
        },
        {
          link: "/svg/sql-svgrepo-com.svg",
          name: "Sql",
        },
        {
          link: "/svg/git-svgrepo-com.svg",
          name: "Git",
        },
        {
          link: "/svg/github-svgrepo-com.svg",
          name: "Github",
        },
        {
          link: "/svg/bitbucket-svgrepo-com.svg",
          name: "Bitbucket",
        },
        {
          link: "/svg/jira-svgrepo-com.svg",
          name: "Jira",
        },
        {
          link: "/svg/vscode-svgrepo-com.svg",
          name: "Vscode",
        },
        {
          link: "/svg/bootstrap-fill-svgrepo-com.svg",
          name: "Bootstrap",
        },
        {
          link: "/svg/tailwind-svgrepo-com.svg",
          name: "Tailwind CSS",
        },
      ],
    };
  },
};
</script>
