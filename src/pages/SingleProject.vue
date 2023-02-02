<template>
  <div>
    <h1>{{ project.title }}</h1>
    <h3>Nome Cliente: {{ project.client_name }}</h3>
    <p>Descrizione del progetto: {{ project.description }}</p>

    <p>Tipologia di progetto:{{ project.type.name }}</p>
    <p>
      Linguaggi/o usato/i:
      <span
        v-for="technology in project.technologies"
        class="badge rounded-pill text-bg-dark"
        >{{ technology.name }}</span
      >
    </p>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "SingleProject",
  data() {
    return {
      project: null,
    };
  },
  created() {
    axios
      .get(`http://127.0.0.1:8000/api/projects/${this.$route.params.slug}`)
      .then((response) => {
        this.project = response.data;
      });
  },
};
</script>

<style lang="scss" scoped></style>
