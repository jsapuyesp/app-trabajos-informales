<template>
  <div id="nav" class="nav">

    <nav class="nav-link">
      <router-link :to="{name : 'Home'}">Inicio</router-link> |
      <router-link :to="{name : 'Profile'}">Perfil</router-link>
    </nav>

    <div class="auth">
    <router-link :to="{name : 'Login'}">Login</router-link> |
    <router-link :to="{name : 'Register'}">Register</router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "NavBar",
  methods: {
  }
};
</script>

<style scoped>
.nav {
  display: flex;
}
.auth {
  margin-left: auto;
}
.nav-link{
  
}
</style>
