<template>
  <div class="skill-listing">
    <div class="btns"></div>
    <section id="foods" class="foods-section">
      <h1
        class="mx-auto text-6xl underline text-center mb-12 font-semibold text-3xl text-green-500 drop-shadow-sm"
      >
        Skills
      </h1>

      <section class="text-gray-900 font-sans p-6">
        <div class="container mx-auto">
          <div class="flex flex-wrap flex-1 -mx-4">
            <div
              v-for="skill in skills"
              :key="skill.id"
              class="w-full sm:w-1/2 md:w-1/2 xl:w-1/4 p-4 itemBox"
            >
              <a
                href="/signup"
                class="c-card block bg-white shadow-md hover:shadow-xl rounded-lg overflow-hidden"
              >
                <div class="relative pb-48 overflow-hidden">
                  <img
                    class="absolute inset-0 h-full w-full object-cover"
                    :src="require('../assets/images/' + skill.title + '.jpeg')"
                    :alt="skill.title"
                  />
                </div>
                <div class="p-4">
                  <span
                    class="inline-block px-2 py-1 leading-none bg-green-300 text-white rounded-full font-semibold uppercase tracking-wide text-xs"
                    >Skill</span
                  >
                  <h2 class="mt-2 mb-2 font-bold">{{ skill.title }}</h2>
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
  name: "Learning",
  props: ["skills"],
  mounted() {
    console.log(this.skills);
  },
};
</script>
