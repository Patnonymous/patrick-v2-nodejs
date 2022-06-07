<template>
  <div class="mb-5">
    <b-navbar toggleable="lg" type="dark" variant="info">
      <b-navbar-brand to="/">Home</b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item :active="isRouteActive('about')" to="/about"
            >About</b-nav-item
          >
          <b-nav-item :active="isRouteActive('projects')" to="/projects"
            >Projects</b-nav-item
          >
          <b-nav-item :active="isRouteActive('contact')" to="/contact"
            >Contact</b-nav-item
          >
          <b-nav-item :active="isRouteActive('resume')" href="/resume.pdf"
            >Resume</b-nav-item
          >
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>



<script>
export default {
  data() {
    return {};
  },
  mounted() {},
  methods: {
    isRouteActive(routeName) {
      return this.$route.fullPath.includes(routeName);
    },
  },
  computed: {},
};
</script>