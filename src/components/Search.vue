<template>
  <div class="search-bar">
    <form action="" @submit="submit($event)">
      <input
        v-model="keyword"
        type="text"
        class="search-field p-3 m-3 font-lg"
        placeholder="Jobs or Skills"
      />
    </form>
  </div>
</template>

<script>
export default {
  name: "Search",
  data() {
    return {
      keyword: "",
    };
  },
  methods: {
    submit(e) {
      e.preventDefault();
      this.$route.push({
        name: "create",
        params: {
          data: {
            keyword: keyword,
          },
        },
      });
    },
  },
};
</script>

<style>
.search-field {
  border-radius: 20px !important;
  border: 1px solid #69be86;
  /* background: #bffbd2; */
  /* color: white !important; */
}
</style>
