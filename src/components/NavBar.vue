<template>
  <b-container fluid>
    <b-navbar type="dark" class="b-navbar">
      <b-navbar-brand :to="{ name: 'Home' }">
        <b-img
          src="https://vuejs.org/images/logo.png?_sw-precache=cf23526f451784ff137f161b8fe18d5a"
          style="max-width: 50px"
          fluid
          alt="Responsive image"
        ></b-img>
      </b-navbar-brand>
      <b-navbar-nav style="margin-left: auto">
        <b-nav-item :to="{ name: 'Home' }">Home</b-nav-item>

        <!-- Navbar dropdowns -->
        <b-nav-item-dropdown text="User" right>
          <b-dropdown-item :to="{ name: 'Profile' }">Profile</b-dropdown-item>
          <b-dropdown-item :to="{ name: 'Login' }">Login</b-dropdown-item>
          <b-dropdown-item :to="{ name: 'Register' }">Register</b-dropdown-item>
        </b-nav-item-dropdown>
      </b-navbar-nav>
    </b-navbar>
  </b-container>
</template>

<script>
export default {
  name: "NavBar",
  methods: {},
  computed: {},
};
</script>

<style scoped>
.container-fluid {
  padding-left: 0px;
  padding-right: 0px;
}
.b-navbar {
  background-color: #333333;
}
</style>
