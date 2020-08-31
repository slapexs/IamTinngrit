<template>
  <div>
    <nav
      class="navbar is-fixed-top"
      role="navigation"
      aria-label="main navigation"
    >
      <div class="container">
        <div class="navbar-brand">
          <nuxt-link to="/" class="navbar-item">
            <img
              src="~/static/onze_favicon.png"
              height="32"
              draggable="false"
            />
            <span class="ml-2">ONZE</span>
          </nuxt-link>

          <a
            role="button"
            class="navbar-burger burger"
            aria-label="menu"
            aria-expanded="false"
            data-target="mainNavbar"
            @click="showNav = !showNav"
            :class="{ 'is-active': showNav }"
          >
            <span aria-hidden="true"></span>
            <span aria-hidden="true"></span>
            <span aria-hidden="true"></span>
          </a>
        </div>

        <div
          id="mainNavbar"
          class="navbar-menu"
          :class="{ 'is-active': showNav }"
        >
          <div class="navbar-start">
            <a href="#about" class="navbar-item">About me</a>
            <a href="#skill" class="navbar-item">Skill</a>
            <a href="#social" class="navbar-item">Social</a>
          </div>
          <div class="navbar-end">
            <!-- <nuxt-link to="/work" class="navbar-item">Works</nuxt-link>
            <nuxt-link to="/blog" class="navbar-item">Blogs</nuxt-link> -->

            <nuxt-link to="/githubprofile" class="navbar-item"
              >Github profile</nuxt-link
            >
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>
<script>
export default {
  data() {
    return {
      showNav: false,
    }
  },
}
</script>
