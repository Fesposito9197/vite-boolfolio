<script>
import ListProject from "./ListProject.vue";
export default {
  name: "AppMain",
  components: { ListProject },
};
</script>

<template>
  <main>
    <router-view></router-view>
  </main>
</template>

<style lang="scss" scoped></style>
