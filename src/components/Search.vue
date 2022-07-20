<template>
  <div class="search-bar">
    <form action="">
      <input
        type="text"
        class="container text-left -ml-1 mt-8 w-3/4 h-12 bg-gray-100 border-2 border-green-500 rounded-xl pl-4"
        placeholder="Content Writer"
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
