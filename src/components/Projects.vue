<template>
  <section>
    <SectionTitle title="Projects" sectionID="projects" />

    <div
      class="grid gap-8 lg:grid-cols-2 sm:max-w-sm sm:mx-auto lg:max-w-full text-gray-400"
    >
      <div
        v-for="(project, index) in projects"
        :key="index"
        class="px-3 py-5 shadow-sm shadow-green-400 rounded overflow-hidden"
      >
        <div>
          <div class="mb-2">
            <a
              href="/"
              aria-label="Article"
              class="inline-block text-2xl font-bold leading-5 transition-colors duration-200"
              >{{ project.title }}</a
            >
          </div>
          <p class="mb-5 h-36 md:h-24 overflow-y-auto">
            {{ project.details }}
          </p>
          <div class="flex justify-end gap-3">
            <!-- Github -->
            <a
              v-if="project.git"
              :href="project.git"
              target="_blank"
              class="px-2 py-1 flex items-center rounded border border-green-400 text-sm"
            >
              <img src="/svg/github-svgrepo-com.svg" class="h-5 w-5" alt="" />
            </a>
            <!-- Github Ends -->
            <!-- Web -->
            <a
              v-if="project.web"
              :href="project.web"
              target="_blank"
              class="px-2 py-1 flex items-center rounded border border-green-400 text-sm"
            >
              <img
                src="/svg/internet-explorer-logo-svgrepo-com.svg"
                class="h-5 w-5"
                alt=""
              />
            </a>
            <!-- Web Ends -->
            <!-- <span
              class="px-2 py-1 flex items-center rounded border border-green-400 text-sm"
            >
              Read More
            </span> -->
          </div>
        </div>
      </div>
    </div>
  </section>
  <div class="py-6"></div>
</template>
<script>
import SectionTitle from "./SectionTitle.vue";
export default {
  data() {
    return {
      projects: [
        {
          title: "Finance Tracker/Logger",
          details:
            "Finance Tracker/Logger helps users track daily income, expenses and saving for different accounts and also outputs results via lists and charts",
          languages: ["JavaScript", "Vue Js", "Php", "Laravel"],
          git: "https://github.com/codeDeeAi/financeloggerclient",
          web: "https://finance-logger-client.herokuapp.com/",
          video: "",
        },
        {
          title: "Hulo (Realtor's portal)",
          details:
            "Real estate marketplace (PWA) aimed at connecting verified house owners and realtor to prospective buyers. created with Nuxt Js, Laravel , Amazon S3",
          languages: [
            "JavaScript",
            "Vue Js",
            "Nuxt Js",
            "Php",
            "Laravel",
            "SQL",
            "AWS S3",
          ],
          git: "",
          web: "http://hulo-2.herokuapp.com/",
          video: "",
        },
        {
          title: "Hulo (Buyer)",
          details:
            "Real estate marketplace (PWA) aimed at connecting verified house owners and realtor to prospective buyers. created with Nuxt Js, Laravel , Amazon S3",
          languages: [
            "JavaScript",
            "Vue Js",
            "Nuxt Js",
            "Php",
            "Laravel",
            "SQL",
            "AWS S3",
          ],
          git: "",
          web: "http://hulo-1.herokuapp.com/",
          video: "",
        },
        {
          title: "Issue/Bug Tracker",
          details:
            "Issue/Bug Tracker for recording bugs/defects quality assurance testers. Manage Teams, Assign Tasks & Export to excel sheet",
          languages: ["JavaScript", "Vue Js", "Php", "Laravel"],
          git: "https://github.com/codeDeeAi/issue_tracker.git",
          web: "",
          video: "/videos/bugtracker.mp4",
        },
        {
          title: `Adriano's home`,
          details: "A portfolio, blog and mini ecommerce store ",
          languages: ["JavaScript", "Vue Js", "Php", "Laravel"],
          git: "",
          web: "https://adrianoolatigbe.com",
        },
        {
          title: "Vue Js Windows History Buttons",
          details:
            "A highly customizable Vue Js 3 plugin for controlling browser history pages (next and previous)",
          languages: ["JavaScript", "Vue Js"],
          git: "https://github.com/codeDeeAi/vue-window-history-control-buttons.git",
          web: "",
        },
        {
          title: "Get Jokes Page",
          details:
            "A simple webpage with  HTML, CSS, Tailwind Css, JavaScript, and Vue Js that gets jokes from an open source API based on the user's preferred filter",
          languages: ["JavaScript", "Vue Js"],
          git: "https://github.com/codeDeeAi/get_jokes_from_open_source_api.git",
          web: "https://nifty-varahamihira-b5b934.netlify.app",
        },
        {
          title: "OneHourToDo Application",
          details:
            "A Project Based on a challenge to build a ToDo App with Laravel and Vue Js in One Hour",
          languages: ["Laravel 8", "Vue Js", "Sql"],
          git: "https://github.com/codeDeeAi/ToDoApp.git",
          web: "",
          video: "/videos/todo.mp4",
        },
        {
          title: "LaraBlog",
          details:
            "      A Blog web app with Laravel and Vue Js, it has some very important and unique features, most importantly it can be fully customized by the administrator. It also features user roles and permission at the admin panel",
          languages: ["Laravel 7", "Vue Js", "Sql"],
          git: "https://github.com/codeDeeAi/Larablog.git",
          web: "",
          video: "/videos/larablog.mp4",
        },
        {
          title: "TFLM",
          details: "An NGO and Ministry web app with Php and Javascript",
          languages: ["JavaScript", "Php", "Sql"],
          git: "https://github.com/codeDeeAi/TFLM.git",
          web: "",
          video: "/videos/tflm.mp4",
        },
        {
          title: "KYC Loan App",
          details:
            "An app designed with Php, which shows the simple process of loan verification of a bank XYZ",
          languages: ["JavaScript", "Php", "Sql"],
          git: "https://github.com/codeDeeAi/kyc-loan-app.git",
          web: "",
          video: "/videos/xyz.mp4",
        },
        {
          title: "RyseHub",
          details:
            "A simple functional e-commerce web app with just HTML, CSS, bootstrap, JavaScript, VueJS and Firebase ",
          languages: ["JavaScript", "Vue Js", "Firebase"],
          git: "",
          web: "http://www.rysehub.com.ng",
        },
        {
          title: "Twitter",
          details:
            "A simple recreation of twitter's landing page with just HTML, CSS, bootstrap and Simple JavaScript",
          languages: ["JavaScript"],
          git: "https://github.com/codeDeeAi/Twitter.git",
          web: "https://xenodochial-curran-dc0dce.netlify.app",
        },
        {
          title: "Diamond Bridge of Desmond",
          details:
            "Construction company webpage with  HTML, CSS,  JavaScript, Vue Js and Materialize CSS ",
          languages: ["JavaScript", "Vue Js"],
          git: "",
          web: "https://www.diamondbridgeofdesmond.com",
        },
      ],
    };
  },
  components: { SectionTitle },
};
</script>
