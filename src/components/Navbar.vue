<template>
  <div
    class="navbar py-8 px-6 md:flex justify-between items-center"
    :class="[open ? '' : 'shadow']"
  >
    <div class="brand px-12 flex items-center cursor-pointer font-semibold">
      <img src="../assets/images/logo.png" id="brand-img" alt="" srcset="" />
    </div>

    <span
      @click="menuOpen()"
      class="absolute md:hidden right-6 top-5 cursor-pointer text-4xl"
    >
      <i :class="[open ? 'bi bi-x' : 'bi bi-filter-left']"></i>
    </span>

    <ul
      class="nav-links md:flex md:items-center md:px-0 px-10 md:pb-0 pb-10 md:static absolute md:w-auto w-full top-24 duration-500 ease-in"
      :class="[open ? 'left-0 shadow' : 'left-[-100%]']"
    >
      <li class="md:mx-4 md:my-0 my-6" v-for="link in links" :key="link.id">
        <a
          :href="link.link"
          class="nav-link text-xl hover:text-green-500 cursor-pointer"
          >{{ link.name }}</a
        >
      </li>
    </ul>
    <!-- 
    <ButtonComp>
    </ButtonComp> -->
  </div>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      open: false,
      links: [
        { name: "Home", link: "/" },
        { name: "About", link: "/about" },
        { name: "Jobs", link: "#jobs" },
        { name: "Contact", link: "/contact" },
      ],
    };
  },
  methods: {
    menuOpen() {
      this.open = !this.open;
    },
  },
};
</script>

<style scoped lang="scss">
$primary-color: #69be86;
$bg-color: #fcfcfc;
.navbar,
.nav-links,
.nav-link {
  //   background: $bg-color !important;
}

.nav-link {
  color: $primary-color;
}

#brand-img {
  width: 80px;
  height: 50px;
}
</style>
