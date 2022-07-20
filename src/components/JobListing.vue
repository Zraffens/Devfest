<template>
  <div class="job-listing">
    <div class="btns"></div>
    <section id="foods" class="foods-section">
      <h1
        class="mx-auto text-6xl underline text-center mb-12 font-semibold text-3xl text-green-500 drop-shadow-sm"
      >
        Jobs
      </h1>
      <ul class="flex w-4/5 mx-auto">
        <li
          @click="filter('All')"
          class="tag btn rounded-md list active inline flex-1 text-center p-4"
          data-filter="list rounded-md cursor-pointer flex-1 mx-8 text-center p-4 text-green-800 bg-white hover:text-white hover:bg-green-800 border-gray-400 tag"
        >
          All
        </li>
        <li
          v-for="job in jobs"
          :key="job.id"
          @click="filter(job.tag)"
          class="list rounded-md cursor-pointer flex-1 mx-8 text-center p-4 text-green-800 bg-white hover:text-white hover:bg-green-800 border-gray-400 tag"
          data-filter="{{job.tag}}"
        >
          {{ job.tag }}
        </li>
      </ul>

      <section class="text-gray-900 font-sans p-6">
        <div class="container mx-auto">
          <div class="flex flex-wrap flex-1 -mx-4">
            <div
              v-for="job in filteredJobs"
              :key="job.id"
              class="w-full sm:w-1/2 md:w-1/2 xl:w-1/4 p-4 itemBox"
              :id="job.tag"
            >
              <a
                href="/signup"
                class="c-card block bg-white shadow-md hover:shadow-xl rounded-lg overflow-hidden"
              >
                <div class="relative pb-48 overflow-hidden">
                  <img
                    class="absolute inset-0 h-full w-full object-cover"
                    :src="require('../assets/images/' + job.img + '.jpeg')"
                    :alt="job.title"
                  />
                </div>
                <div class="p-4">
                  <span
                    class="inline-block px-2 py-1 leading-none bg-green-300 text-white rounded-full font-semibold uppercase tracking-wide text-xs"
                    >Job</span
                  >
                  <h2 class="mt-2 mb-2 font-bold">{{ job.title }}</h2>
                </div>
              </a>
            </div>
          </div>
        </div>
      </section>
    </section>
  </div>
</template>

<script>
export default {
  name: "JobListing",
  props: ["jobs"],
  data() {
    return {
      filteredJobs: [],
    };
  },
  mounted() {
    this.filteredJobs = this.jobs;
  },
  methods: {
    filter(tag) {
      if (tag === "All") {
        this.filteredJobs = this.jobs;
      } else {
        this.filteredJobs = this.jobs.filter((item) => {
          return item.tag === tag;
        });
      }
      document.getElementById(tag).classList += 'active'
    },
  },
};
</script>

<style>
.tag {
  border: 1px solid #ccc;
  transition: 0.3s ease-in-out;
}
</style>
