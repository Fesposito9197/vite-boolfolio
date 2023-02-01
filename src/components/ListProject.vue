<template>
  <section>
    <h1 class="text-center">lista progetti</h1>
    <div class="container">
      <div class="row gy-3">
        <div class="col-md-4" v-for="project in projects">
          <ProjectCard :data="project" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import axios from "axios";
import ProjectCard from "./ProjectCard.vue";
export default {
  name: "ListProject",
  components: {
    ProjectCard,
  },
  data() {
    return {
      projects: [],
    };
  },
  created() {
    axios.get("http://127.0.0.1:8000/api/projects").then((response) => {
      this.projects = response.data;
    });
  },
};
</script>

<style lang="scss" scoped></style>
