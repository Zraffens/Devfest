<template>
  <nav>
    <Navbar />
  </nav>

  <router-view v-slot="{ Component }">
    <transition name="view">
      <component :is="Component"></component>
    </transition>
  </router-view>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
export default {
  name: "App",
  components: {
    Navbar,
  },
};
</script>

<style lang="scss" scoped>
.view-enter-active,
.view-leave-active {
  transition: opacity 0.5s ease;
}

.view-enter-from,
.view-leave-to {
  opacity: 0;
}
</style>
