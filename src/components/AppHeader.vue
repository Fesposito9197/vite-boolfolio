<script>
export default {
  name: "AppHeader",
};
</script>
<template>
  <h1>Header</h1>
  <nav>
    <ul>
      <li><RouterLink to="/">HomePage</RouterLink></li>
      <li><RouterLink to="about-us">About Us</RouterLink></li>
      <li><RouterLink to="contact-us">Contact Us</RouterLink></li>
    </ul>
  </nav>
</template>

<style lang="scss" scoped></style>
