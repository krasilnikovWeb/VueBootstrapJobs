<template>
  <div>
    <!-- class="p-1" -->
    <b-navbar toggleable="lg" type="dark" variant="info">
      <b-navbar-brand class="ms-1" href="#">NavBar</b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item to="/">Home</b-nav-item>
          <b-nav-item to="/about">About</b-nav-item>
        </b-navbar-nav>

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ms-auto me-1">
          <b-nav-form class="me-1">
            <b-form-input
              size="sm"
              placeholder="Search"
              v-model="searchText"
            ></b-form-input>
          </b-nav-form>
          <!-- m-1 -->
          <b-button @click="search" size="sm" type="submit">Search</b-button>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  methods: {
    search() {
      this.$store.dispatch("search", { text: this.searchText });
    },
  },
  data() {
    return {
      searchText: "",
    };
  },
};
</script>

<style lang="scss" scoped>
#nav a.router-link-exact-active {
  color: white;
}
</style>
