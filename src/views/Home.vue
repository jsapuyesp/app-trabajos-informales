<template>
  <div class="home">
    <h1>Home</h1>
    <p v-if="userLogged">User loggued: {{ userLogged }}</p>
  </div>
</template>

<script>
import auth from "@/logic/auth";
export default {
  name: "Home",
  components: {
    
  },
  computed: {
    userLogged() {
      return auth.getUserLogged();
    },
  },
};
</script>

<style></style>
