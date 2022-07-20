<template>
  <div class="search-bar">
    <form action="">
      <input
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
