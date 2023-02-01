<template>
  <div class="card">
    <img
      v-if="data.image_url"
      :src="data.image_url"
      class="card-img-top"
      :alt="data.title"
    />
    <div class="card-body">
      <h5 class="card-title">{{ data.title }}</h5>
      <p class="card-text">
        {{ truncateText(data.description) }}
      </p>
      <!-- <a href="#" class="btn btn-primary">Go somewhere</a> -->
    </div>
  </div>
</template>

<script>
export default {
  name: "ProjectCard",
  props: {
    data: Object,
  },
  methods: {
    truncateText(text) {
      return text.substring(0, 250) + "...";
    },
  },
};
</script>

<style lang="scss" scoped></style>
