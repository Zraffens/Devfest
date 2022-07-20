<template>
  <div class="search">
    <h1 class="text-5xl">Search Results for {{ $route.params.keyword }}:</h1>
  </div>
</template>

<script>
export default {
  name: "SearchVue",
  props: ["keyword", "jobs", "skills"],
};
</script>

<style></style>
