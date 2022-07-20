<template>
  <div class="job-listing">
    <h1 class="5-xl">Job Listing</h1>
    <div class="btns"></div>
    <section id="foods" class="foods-section">
      <h1
        class="mx-auto mb-12 font-semibold text-3xl text-[#dd7230] drop-shadow-sm"
      >
        Skills to learn
      </h1>
      <ul class="">
        <li class="list active" data-filter="all">All</li>
        <li
          v-for="job in skills"
          :key="job.id"
          class="list"
          data-filter="{{job.tag}}"
        >
          {{ job.tag }}
        </li>
      </ul>

      <section class="text-gray-900 font-sans p-6">
        <div class="container mx-auto">
          <div class="flex flex-wrap flex-1 -mx-4">
            <div
              v-for="job in skills"
              :key="job.id"
              class="w-full sm:w-1/2 md:w-1/2 xl:w-1/4 p-4 itemBox"
              data-item="job.tag"
            >
              <a
                href=""
                class="c-card block bg-white shadow-md hover:shadow-xl rounded-lg overflow-hidden"
              >
                <div class="relative pb-48 overflow-hidden">
                  <img
                    class="absolute inset-0 h-full w-full object-cover"
                    src="{{job.img}}"
                    :alt="job.title"
                  />
                </div>
                <div class="p-4">
                  <span
                    class="inline-block px-2 py-1 leading-none bg-green-300 text-white rounded-full font-semibold uppercase tracking-wide text-xs"
                    >Lunch</span
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
  props: ["skills"],
};
</script>

<style></style>
