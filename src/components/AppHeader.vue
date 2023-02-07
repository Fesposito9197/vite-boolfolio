<script>
export default {
  name: "AppHeader",
};
</script>
<template>
  <header class="bg-primary bg-gradient">
    <div class="container">
      <nav class="navbar navbar-expand-lg bg-body-tertiary">
        <div class="container-fluid">
          <button
            class="navbar-toggler"
            type="button"
            data-bs-toggle="collapse"
            data-bs-target="#navbarNav"
            aria-controls="navbarNav"
            aria-expanded="false"
            aria-label="Toggle navigation"
          >
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav">
              <li class="nav-item">
                <RouterLink
                  :to="{ name: 'homepage' }"
                  class="nav-link text-white"
                >
                  HomePage
                </RouterLink>
              </li>
              <li class="nav-item">
                <RouterLink
                  :to="{ name: 'about-us' }"
                  class="nav-link text-white"
                >
                  About Us
                </RouterLink>
              </li>
              <li class="nav-item">
                <RouterLink
                  :to="{ name: 'contact-us' }"
                  class="nav-link text-white"
                >
                  Contact Us
                </RouterLink>
              </li>
            </ul>
          </div>
        </div>
      </nav>
    </div>
  </header>
</template>

<style lang="scss" scoped></style>
