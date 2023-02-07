<template>
  <div class="container">
    <div class="container d-flex justify-content-center text-center">
      <div class="card mt-5" style="width: 30rem">
        <img
          :src="project.image_url"
          class="card-img-top img-fluid"
          :alt="project.title"
        />
        <div class="card-body">
          <h5 class="card-title">{{ project.title }}</h5>
          <p class="card-text">
            {{ project.description }}
          </p>
          <span
            v-for="technology in project.technologies"
            class="badge rounded-pill text-bg-dark ms-2"
          >
            {{ technology.name }}
          </span>
        </div>
      </div>
    </div>

    <!-- <img :src="project.image_url" alt="" />
    <h1>{{ project.title }}</h1>
    <h3>
      Nome Cliente: <span>{{ project.client_name }}</span>
    </h3>
    <p>Descrizione del progetto: {{ project.description }}</p>

    <p>Tipologia di progetto:{{ project.type?.name }}</p>
    <p>
      Linguaggi/o usato/i:
      <span
        v-for="technology in project.technologies"
        class="badge rounded-pill text-bg-dark ms-2"
        >{{ technology.name }}</span
      >
    </p> -->
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "SingleProject",
  data() {
    return {
      project: [],
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
